Principio Inversión de Dependencias (DIP)
El principio se implementa en este con:

1. **Uso de una abstracción como contrato (`EnvioRecibo`):** Se define una clase abstracta con un método virtual puro (`virtual void EnviarRecibo(...) = 0`), lo que permite que los módulos de alto nivel dependan de una interfaz general y no de implementaciones específicas.
2. **Inyección de dependencias mediante la interfaz (`AdmProducto`):** La clase `AdmProducto` no depende de clases concretas de bajo nivel, sino que recibe la abstracción `EnvioRecibo` en su método, permitiendo intercambiar o inyectar distintas formas de envío (como `EnviarEmail` o `EnviarApp`) sin acoplar el código.
