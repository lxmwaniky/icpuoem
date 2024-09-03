The DFX SDK is the development toolkit that allows you to build, deploy, and manage applications on the Internet Computer. It manages canisters, cycles, and connections to the ICP network.

## Installation
- To install it, you can follow these steps:
```bash
sh -ci "$(curl -fsSL https://internetcomputer.org/install.sh)"
```
- Verify the Installation
```bash
dfx --version
```

## Syntax
- The DFX SDK uses the following syntax:
```bash
dfx [subcommand] [flag]
```
### Subcommands
The following is a list of the essential dfx subcommands that you'll be using:

`dfx start` - Starts the local Internet Computer replica.

`dfx stop` - Stops the local Internet Computer replica.

`dfx build` - Builds a canister project.

`dfx deploy` - Deploys a canister to the local Internet Computer replica.

`dfx canister` - Manages canisters on the local Internet Computer replica.

`dfx ledger` - Manages cycles on the local Internet Computer replica.

`dfx identity` - Manages the identity of the local Internet Computer replica.

`dfx help` - Displays help information for the DFX SDK.

`dfx --version` - Displays the version of the DFX SDK.

`dfx ping` - Pings the local Internet Computer replica.

### Flags

`-h`, `--help`: Used to display usage information.

`-q`, `--quiet`: Used to suppress informational messages.

`-v`, `--verbose`: Used to display detailed information about operations.

`-V`, `--version`: Used to display the version of dfx installed.

Next Section: [Creating a new project](./NEW-PROJECT.md)
