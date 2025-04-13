# Comandos Básicos de Foundry

## 1. Inicialización y Configuración
- `forge init` → Inicializa un nuevo proyecto Foundry.
- `forge install <dependencia>` → Instala una dependencia (ej: `forge install OpenZeppelin/openzeppelin-contracts`).
- `forge update` → Actualiza las dependencias.

## 2. Compilación
- `forge build` → Compila los contratos.
- `forge clean` → Elimina archivos compilados y caché.

## 3. Testing
- `forge test` → Ejecuta todos los tests.
- `forge test --match <nombre_test>` → Ejecuta tests específicos (ej: `--match testDeposit`).
- `forge test -vvv` → Muestra logs detallados (niveles de verbosidad: `-v` a `-vvvv`).

## 4. Despliegue (Deploy)
- `forge create <contrato>` → Despliega un contrato (ej: `forge create src/MyContract.sol:MyContract`).
- `forge script <script>` → Ejecuta un script de deploy (ej: `forge script script/Deploy.s.sol`).
  - Con variables de entorno:  
    ```bash
    forge script script/Deploy.s.sol --private-key $PRIV_KEY --rpc-url $RPC_URL
    ```

## 5. Interacción con Contratos
- `forge cast` → Para llamadas a contratos desplegados.
  - Ejemplo:  
    ```bash
    cast send <dirección_contrato> "funcion()" --private-key $PRIV_KEY --rpc-url $RPC_URL
    ```

## 6. Verificación
- `forge verify-contract <dirección> <contrato> --etherscan-api-key $ETHERSCAN_KEY` → Verifica un contrato en Etherscan.

## 7. Utilidades
- `forge fmt` → Formatea el código según estándares.
- `forge inspect <contrato> <propiedad>` → Obtiene metadatos (ej: `forge inspect MyContract abi`).

## 8. Ejecución Local (Anvil)
- `anvil` → Inicia una blockchain local para testing (similar a Ganache).

---

# Foundry Zk-Sync

## Instalación
- Para instalarlo tienes que ejecutar este comando (Nota: Funciona en Linux. Windows requieres de WSL):
    ```bash
    curl -L https://raw.githubusercontent.com/matter-labs/foundry-zksync/main/install-foundry-zksync | bash
    ```
- `foundryup-zksync` → Actualiza y habilita comandos relacionados con Zk-Sync.
- `foundryup` → Devuelve a foundry vanilla e inhabilita comandos relacionados con Zk-Sync.

## Documentation

https://book.getfoundry.sh/
https://foundry-book.zksync.io/getting-started/installation
