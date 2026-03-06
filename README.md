# Entornos-7.2
Repo para Diagramas de Casos de Uso

# 1. Sistema de Iluminación Inteligente

```mermaid
graph LR
%% Definir el Actor 
Usuario((Usuario))
%% Definir límite del Sistema
subgraph "Aplicación de Iluminación"
CU1([Encender Luces])
CU2([Apagar Luces])
end
%% Definir relaciones Actor/Casos de Uso
Usuario --- CU1
Usuario --- CU2

```


# 2. Gestión de Tienda Online

```mermaid
graph LR
%% Definir Actores
Cliente((Cliente))
Administrador((Administrador))
%% Definir límite del Sistema y Acciones
subgraph "Gestor Tienda Online"
CU1([Comprar Producto])
CU2([Gestionar Stock])
CU3([Aplicar Cupón Descuento])

%% Definir relaciones especiales (extend)

CU3 -.->|&lt;&lt;extend&gt;&gt;| CU1

end

%% Definir relaciones Actor/Casos de Uso
Cliente --- CU1
Administrador --- CU2


```


# 3. Plataforma de Streaming

```mermaid


```


