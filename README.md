# W3M-Bootcamp
Recursos para el bootcamp de [Web3Makers](https://web3makers.org)

![](https://lh3.googleusercontent.com/drive-viewer/AJc5JmQ7VnLur8l35c4hvidKWexnMQpbLSXUxkSh7qTjvWisEdbLrw3Wa742BiqMpJ8znmWurlKdVEE=w1778-h1880)

# Introducción

## ¿Por qué Smart Contracts?

> Nos permiten crear sistemas que faciliten acuerdos donde la necesidad de confianza es minimizada.
    
### ¿Como minimizan la necesidad de confianza?

1. **Inmutabilidad**: una vez desplegados en una blockchain, no pueden ser cambiados.
2. **Transparencia**: todas las interacciones quedan almacenadas en una blockchain, lo que nos da trazabilidad.
3. **Resiliencia**: mientras funcione la blockchain, funcionan los contratos. Heredan la seguridad y resiliencia de la blockchain sobre la que corren.

## Desventajas de los Smart Contracts
1. **Costo**: debido al alto nivel de redundancia que poseen las blockchains más seguras
2. **Transparencia**: todas las interacciones quedan almacenadas en una blockchain, haciendo casos de uso donde la privacidad es necesaria más difíciles de implementar
3. **Madurez tecnológica**: es una tecnología que se encuentra en desarrollo activo y muchas de las herramientas y prácticas experimentan cambios frequentes

## Como crear y usar Smart Contracts

Como mencionamos previamente los Smart Contracts se alojan sobre una blockchain. No todas las blockchains (Bitcoin por ejemplo) tiene soporte para Smart Contracts. Ethereum fue la primera red en implementarlos a través de la Ethereum Virtual Machine (EVM) que maneja todas las transacciones de la red y tiene funciones especiales que permiten que sus transacciones no solo transmitan ETH, si no que tambíen permite subir programas, los cuales tienen su propia dirección y pueden recibir transacciones conteniendo datos para llamar a las funciones del programa.

- [Ethereum Stack](https://ethereum.org/en/developers/docs/ethereum-stack/)

## Ejemplos de uso de Smart Contracts

### Tokens

La forma más común de clasificar los tokes es según su fungibilidad:

**Tokens Fungibles:** cada unidad de un token fungible tiene el mismo valor y las mismas características que cualquier otra unidad del token.

Son comúnmente utilizados como medios de intercambio. Algúnos ejemplos pueden ser ETH, BTC, USDT, DOGE, UNI.

Para implementar este tipo de tokens se suele usar un estandar llamado **ERC-20** que es un contrato que implementa las funciones definidas en el estandard.
- [Documentación](https://ethereum.org/en/developers/docs/standards/tokens/erc-20/)

**Tokens No Fungibles (NFT):** en cambio, para los NFTs, cada unidad puede tener un valor distinto y caraterísticas unicas.

Normalmente suelen estar agrupados en colecciones, como por ejemplo los Crypto Kitties, Bored Apes Yatch Club y Cryptopunks. Pero también pueden existir colecciones de una sola unidad.

El estandar para estos tokens es el **ERC-721**.

- [Documentación](https://ethereum.org/en/developers/docs/standards/tokens/erc-20/)

### DeFi

**Uniswap:** Intercambio de tokens fungibles decentralizado. Funciona con un Automated Market Maker (AMM) que determina las relaciones de precios entre pares de tokens a base de los balances de cada token depositados en el contrato. No solo facilita el servicio de intercambio, si no que también permite que cualquier usuario deposite tokens en el contrato para aumentar la liquidez del intercambio y a cambio de eso es recompensado con parte de las tarifas cobradas a los usuarios que intercambian tokens.
- [Web](https://uniswap.org/)
- [Documentación](https://uniswap.org/developers)

**AAVE:** Protocolo para prestar y tomar prestado tokens. Los prestamistas pueden ganar interés sobre su capital prestado. Mientras tanto, permite que otros usuarios depositen capital en la plataforma en un token como colateral para luego tomar prestamos en otros tokens.
- [Web](https://aave.com/)
- [Documentación](https://docs.aave.com/hub/)

### Otros

**Lens Protocol:** es un conjunto de Smart Contracts que representan perfiles de usuarios e interacciones entre usuarios como *seguir un usuario*, *hacer una publicación*, *referenciar una publicación* y hasta *crear un NFT a partir de una publicación*. Todas estas interacciones forman una estructura de datos de grafos que puede ser leída por todos y cualquier persona con un perfil puede interactuar. Esto permite que se puedan construir una multitud de aplicaciones sobre la misma estructura de datos, a diferencia de lo que pasa con las redes sociales tradicionales en el que solo los dueños de la plataforma tienen acceso y control sobre los datos.

- [Web](https://lens.xyz/)
- [Documentación](https://docs.lens.xyz/docs)

**Tornado Cash:** es una plataforma que a través de [criptografía de cero conocimiento](https://decrypt.co/resources/zero-knowledge-proofs-explained-learn-guide) permite a los usuarios mandar tokens de una dirección a otra sin que ambas direcciones queden vinculadas por la transacción. Es una herramienta que provee de anonimato a sus usuarios, pero debido a su uso en operaciones de lavado de dinero fue sancionada y uno de sus desarrolladores se encuentra actualmente bajo custodia de autoridades del gobierno.

- [Repositorio de GitHub (Archivado)](https://github.com/tornadocash)
- [Docs](https://github.com/tornadocash/docs)

**Dark Forest:** basado en la saga de ["Remembrance of Earth Past"](https://www.goodreads.com/book/show/34569357-remembrance-of-earth-s-past) y el concepto de los [bosques oscuros](https://medium.com/@ChemAndCode/the-dark-forest-theory-a-chilling-solution-to-fermis-paradox-c576fc0a7307) como solución a la paradoja de Fermi, este juego utiliza criptografía de cero conocimiento para ser un juego de estragía en tiempo real que corre sobre una blockchain pública.
- [Web](https://zkga.me/)

# Práctica
Ahora que pasamos de la introducción básica y casos de usos

## Manejando llaves privadas: Metamask
Para interactuar con las diversas blockchains necesitamos tener una dirección. Y para probar que somos los dueños de esa dirección necesitamos una llave privada. Metamask es una aplicación que se encarga de almacenar tu llave privada y a la vez facilitar la interacción con múltiple blockchains.
- [Descargar Metamask](https://metamask.io/download/)
- [Video Instructivo](https://youtu.be/91Lz4D8PpcQ)

### Recursos sugeridos:
- [Criptografía de llave pública (video)](https://www.youtube.com/watch?v=GSIDS_lvRv4)
- [Documentación de Metamask](https://docs.metamask.io/guide/#why-metamask)

## Introducción práctica a Solidity

Para el primer día del bootcamp, teniendo en cuenta la variedad de niveles, proponemos múltiples rutas de familiaridad con la programación y el lenguaje solidity. Presentamos los materiales en este documento y les sugerimos que si pueden comenzar a verlos y probarlos durante la semana, lo hagan. Después, durante el bootcamp van a poder continuar y tener a los mentores para despejar dudas. 

### Niveles
#### **No sé Solidity**
Si no sos programador, o recién estás arrancando con Solidity, podés comenzar por aca.

[Crypto Zombies](https://cryptozombies.io/en/course/) es una plataforma interactiva en la que podés aprender a programar en Solidity a través de pequeñas lecciones escribiendo código en el Navegador. Recomendamos completar las primeras dos lecciones antes del bootcamp.

#### **Sé solidity**
Si ya tenés experiencia con Solidity y haz escrito un par de Smart contracts te proponemos el desafío de comenzar a aprender más sobre seguridad utilizando [Ethernaut](https://ethernaut.openzeppelin.com/).

Tip: antes del evento buscá un poco de Ether de prueba en la red Goerli con los siguientes faucets:
- https://goerlifaucet.com/
- https://faucets.chain.link/
- https://goerli-faucet.pk910.de/

#### **Tengo un nivel avanzado de Solidity y seguridad en Smart Contracts**
Si estás aca, ya sabés bastante y nuesta única recomendación es que aproveches este tiempo para probar cosas nuevas con la ayuda de los mentores.

### Remix IDE
Para ver y escribir Smart Contracts en este Bootcamp vamos a utilizar el IDE de Remix, el cual es Mantenido por la Ethereum Foundation
  
## Deployment
- [Agregar redes en Metamask]()
- [Deployment]()

## Integración
Ejemplo de integración con React y wagmi hooks
- [Repositorio de GitHub](https://github.com/Eyon42/W3M-bootcamp-ejemplo)
- [Video]()

# Recursos

## Herramientas
- [Remix](https://remix.ethereum.org/): Editor de Solidity online.
- [Hardhat](https://hardhat.org/): Framework para desarrollo de Smart Contracs usando javascript para escribir scripts y pruebas.
- [Etherscan](https://etherscan.io/): Explorador de bloques de Ethereum.
- [Tenderly](https://tenderly.co/): Debuggeador y simulador de Smart Contracts.

## Otros recursos
### [Crypto Zombies]((https://cryptozombies.io/))
Una excelente plataforma para aprender a programar en solidity a través de ejercios en un editor de código online. Todo alrededor del objetivo de crear un videojuego de zombies utilizando Smart Contracts.

### [Contratos de OpenZeppelin](https://github.com/OpenZeppelin/openzeppelin-contracts/)
Colección de Smart Contracts mantenidos por [OpenZeppelin](https://www.openzeppelin.com/), una de las principales empresas de seguridad en Smart Contracts. Pueden encontrar los contratos en la capeta `contracts`, ahí pueden entrar a alguna de las subcarpetas como `token` para ver los contratos de la categoría.

### Patrick Collins
Uno de los más grandes educadores de la comunidad blockchain, hace años que hace contenido sobre programación en [su canal de YouTube](https://www.youtube.com/c/PatrickCollins) y además de eso ha hecho dos colaboraciones ENORMES con [FreeCodeCamp](https://freecodecamp.org):

- [Curso de Solidity con Python (16 horas)](https://www.youtube.com/watch?v=M576WGiDBdQ&t=18583s)
- [Curso de Solidity con Javascript (32 horas)](https://www.youtube.com/watch?v=gyMwXuJrbJQ&t=3333s)

### [Ethernaut](https://ethernaut.openzeppelin.com/)
Una serie de desafíos para desafiar y profundizar tu conocimiento sobre el funcionamiento interno de Solidity y como identificar, prevenir (o explotar) fallas de seguridad en Smart Contracts.

### [Smart Contract Security best practices](https://consensys.github.io/smart-contract-best-practices/)
A list of recommendations written by ConsenSys, the team behind Metamask.

## Oportunidades
Ahora que ya estás equipado con un buen punto de partida y muchos recursos, te sugerimos que tomes el siguiente paso y comiences a poner en práctica tus conocimientos.

### Hackathones
Participar de hackathones es una experiencia maravillosa para aprender y poner a prueba tu conocimiento y habilidades. A continuación encontrarás una lista de lugares donde puedes encontrar hackathones online para participar junto con personas de todo el mundo.

- [ETH Global](ethglobal.com/)
- [Gitcoin](https://gitcoin.co/hackathons)
- [Chainlink](https://chain.link/hackathon)
- [Solana](https://solana.com/)
- [Ethereum Foundation](https://ethereum.org/en/community/events/)
- [DoraHacks](https://dorahacks.io/hackathon)
- [Devfolio](https://devfolio.co/hackathons)
- [Devpost](https://devpost.com/hackathons)

### Otras oportunidades
Luego de participar en hackathones y adquirir un poco de experiencia se abrirán muchas puertas.

¿Alguna de las herramientas que usaste tenía bugs o no se ajustaba a tu caso de uso? Entonces esto es una oportunidad perfecta para intentar hacer el cambio y mejorar esta herramienta y hacer una Pull Request para que se incorpore. En este proceso, aunque no logres resolver el problema o tu solucion no sea aceptada, lograrás profundizar tu entendimiento de como funciona la herramienta y el problema que resuleve y mejoraras tus habilidades para trabajar en conjunto con otras personas.

Otra opción es también buscar algún proyecto que esté buscando desarrolladores e intentar incorporarte. Estos proyectos pueden ser de amigos, start-ups, empresas, DAOs y hasta ONG. Lo importante es seguir aprendiendo y dedicarse a aplicar ese conocimiento.

# Feedback

Pueden entrar a [este link](https://forms.gle/KWVSJwwGN8kay8r19) para darnos feedback del bootcamp.
