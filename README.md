# Entorno de Desarrollo de Lightning Network: De Imprudente a Profesional

En este taller abordaremos la evolución del ecosistema de desarrollo de Lightning Network (LN) - desde el reciente pasado imprudente hasta el futuro (esperemos) más seguro y estable. Demostraremos cómo lograr un entorno de desarrollo que sea reproducible, verificable, portátil y confiable.

La implementación del servidor LSP está escrita en nodejs y actúa como una API JSON-RPC sobre HTTP. Se utiliza el marco de pruebas automatizadas mocha para definir nuestras pruebas. La herramienta CLI scaling-lightning se utiliza para crear y destruir nodos locales de Bitcoin y LN, así como para realizar algunos comandos administrativos. Los mocks pueden ser rápidos y fáciles para pruebas unitarias, pero en este taller queríamos demostrar cómo probar software con nodos LN reales.

## Logrando Objetivos del desarrollador Profesional

Para lograr un desarrollo profesional de manera eficiente y efectiva, se deben cumplir varios objetivos clave:

- Inicio Rápido: Es esencial poder comenzar y funcionar rápidamente.
- Reproducibilidad: Asegurar que los procesos sean replicables y consistentes es crucial.
- Operación Real de Nodos LN: Utilizar nodos reales de Lightning Network para pruebas y desarrollo realistas.
- Regtest Bitcoin: Emplear un entorno de regtest de Bitcoin para pruebas controladas.
- Compatibilidad con Integración Continua (CI): Capacidad para integrarse en pipelines automatizados de CI.

## Herramientas Disponibles

- "#Reckless" :zap:

  - Uso directo de la red principal para experimentación.
  - Aunque arriesgado, a veces puede proporcionar información valiosa.

- [Polar](https://github.com/jamaljsr/polar)

  - Interfaz altamente intuitiva.
  - Proporciona un entorno amigable para un inicio rápido.
  - Como una de las primeras herramientas de desarrollo de LN, sigue siendo mantenida activamente.

* [simLN](https://simln.dev/)

  - Simula actividades de pago a través de varias redes de prueba.
  - Genera actividad aleatoria basada en la topología de la red.
  - Útil para pruebas de estrés de aplicaciones habilitadas para Lightning en escenarios con restricciones de liquidez.

* [warnet](https://warnet.dev/)

  - Establece una red de Bitcoin con interconexiones de nodos especificados.
  - Aunque se centra principalmente en pruebas de Bitcoin Core, también admite funcionalidad de Lightning.

* [Scaling Lightning](https://github.com/scaling-lightning/scaling-lightning)

  - Un conjunto de herramientas de prueba integral para evaluar el protocolo de Lightning Network.
  - Facilita la replicación de la red entre desarrolladores utilizando un archivo de red.
  - Características adecuadas para pruebas automatizadas de extremo a extremo, lo que lo hace adecuado para la integración de CI.

## Redes de Bitcoin

1. Mainnet
   Descripción: Es la red principal de Bitcoin donde se realizan transacciones reales con valor monetario. Aquí es donde se lleva a cabo la actividad económica real y donde los bitcoins tienen valor.
   Uso: Se utiliza para transacciones reales entre usuarios. Cualquier transacción que se realice en Mainnet es irreversible y tiene implicaciones financieras. Es la red que se utiliza para comprar, vender y almacenar bitcoins.
2. Testnet
   Descripción: Es una red de prueba que simula el funcionamiento de la Mainnet, pero sin valor monetario. En Testnet, los bitcoins no tienen valor real y se utilizan para pruebas y desarrollo.
   Uso: Ideal para desarrolladores que quieren probar aplicaciones, wallets o cualquier funcionalidad relacionada con Bitcoin sin arriesgar dinero real. Los usuarios pueden obtener bitcoins de Testnet de manera gratuita a través de faucets (grifos) para realizar pruebas.
3. Regtest
   Descripción: Es una red de prueba que permite a los desarrolladores crear un entorno controlado y privado para probar sus aplicaciones. A diferencia de Testnet, en Regtest, los usuarios pueden generar bloques a voluntad y no hay necesidad de esperar a que se minen.
   Uso: Se utiliza principalmente para el desarrollo y pruebas locales. Permite a los desarrolladores simular situaciones específicas y probar su software en un entorno que pueden controlar completamente, sin la necesidad de conectarse a una red pública.

### Resumen

- Mainnet: Red principal para transacciones reales con valor.
- Testnet: Red de prueba para desarrollos sin valor monetario.
- Regtest: Red de prueba local y controlada para desarrolladores.

## Polar

### Pasos de Demostración de Polar

1. Crear una red
1. Comprar contenedores docker
1. Agregar par
1. Verificación del saldo de la billetera
1. Obtener fondos en la billetera: "lncli newaddress p2wkh"
1. Apertura manual de canal
1. Apertura de canal programada (index.js)
1. Pago de factura Bolt11

### Exportar red de polar

1. Exportar desde la red
1. Analizar los datos exportados
