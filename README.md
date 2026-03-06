# Entornos-7.2
Repo para Diagramas de Casos de Uso

# 1. Sistema de Iluminación Inteligente

```mermaid
graph LR
%% Definir el Actor 
Usuario((Usuario))

%% Definir límite del Sistema y Casos de Uso
subgraph "Aplicación de Iluminación"
CU1([Encender Luces])
CU2([Apagar Luces])
end

%% Definir relaciones Actor-Casos de Uso
Usuario --- CU1
Usuario --- CU2

```

# 2. Gestión de Tienda Online

```mermaid
graph LR
%% Definir Actores
Cliente((Cliente))
Administrador((Administrador))

%% Definir límite del Sistema y Casos de Uso
subgraph "Gestor Tienda Online"
CU1([Comprar Producto])
CU2([Gestionar Stock])
CU3([Aplicar Cupón Descuento])

%% Definir relaciones especiales

%% Relación extend (opcional)
CU3 -.->|&lt;&lt;extend&gt;&gt;| CU1
end

%% Definir relaciones Actor-Casos de Uso
Cliente --- CU1
Administrador --- CU2

```

# 3. Plataforma de Streaming

```mermaid
graph LR
%% Definir Actores
Espectador((Espectador))
EditorDeContenido((EditorDeContenido))
%% Definir Sistema Externo
PasarelaDePagos((PasarelaDePagos))


%% Definir límite del Sistema y Acciones
subgraph "Plataforma de Streaming"
CU1([Reproducir Película])
CU2([Validar Suscripción])
CU3([Activar Subtítulos])
CU4([Subir Nuevo Vídeo])
CU5([Renovar Suscripción])


%% Definir relaciones especiales (include y extend)

%% Relación include (obligatoria) entre Validar Suscripción y Reproducir Película
CU1 -.->|&lt;&lt;include&gt;&gt;| CU2

%% Relación extend (opcional) entre Activar Subtítulos y Reproducir Película
CU3 -.->|&lt;&lt;extend&gt;&gt;| CU1

end

%% Definir relaciones Actor/Casos de Uso
Espectador --- CU1
Espectador --- CU5
EditorDeContenido --- CU4
PasarelaDePagos --- CU5

```

