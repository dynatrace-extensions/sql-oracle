# SQL Oracle Extension
**This is intended for users, who:**
- would like to monitor health state and performance of Oracle database. Dynatrace automatically detects all applications and microservices deployed in your system and how it uses Oracle database. It provides automatic end-to-end tracing down to the single SQL statement, Oracle server metrics and log insights. Dynatrace diagnoses anomalies in real time with AI and pinpoints the root-cause down to the slow performing or erroneous SQL statements. Deep code-level insights combined with cloud native database server monitoring will help you ensure a robust production environment.

**The extension package contains:**
- Monitor infrastructure with a comprehensive dashboard
- Detect traffic anomalies and alert on them
- Topology definition and entity extraction rules.

**Collected metrics:**

CPU
- CPU cores
- Background CPU
- Background CPU usage per core
- Foreground CPU
- Foreground CPU usage per core
- Host CPU usage
- Host CPU usage per core
- Foreground CPU usage per core

Memory
- PGA aggregate limit
- PGA aggregate target
- PGA used for work areas
- PGA memory used
- Allocated PGA
- Shared pool free
- Redo log space wait time
- Redo size increase
- Redo write time
- Buffer cache hit ratio
- Sorts in memory ratio
- Target to limit ratio
- Logical reads
- Physical reads
- Physical reads direct
- Sorts in memory
- Sorts on disk
- Library cache hit ratio

I/O
- Physical read bytes
- Physical byte written
- Total wait time

Query execution
- Connection management time
- PL SQL exec time
- SQL exec time
- SQL parse time
- DB Time
- DB CPU
- Time spent on other activities

Tablespaces
- Total space
- Free space
- Used space
- Used space ratio

Sessions
- Active Sessions
- Total sessions
- User calls
- Sessions limit
- Sessions to limit ratio
- Processes limit

Wait states
- Number of wait events
- Seconds waited

ASM
- ASM - Free space
- ASM - Total space
- ASM - Used space
- ASM - Reads
- ASM - Writes

## Usage
For now go for [dev](#dev)

## Dev

### Prerequisites
- Nix-capable environment, for Windows that means [installing WSL](https://docs.microsoft.com/en-us/learn/modules/get-started-with-windows-subsystem-for-linux/2-enable-and-install)
- [nix](https://nixos.org/download.html) / [**nix for WSL**](https://nixos.org/download.html#nix-install-windows)
- Docker (available in the same environment as nix, required for running companions)

Hint: if something doesn't work because of missing package please add the package to `default.nix` instead of installing on your computer. Why solve the problem for one if you can solve the problem for all? ;)

### Everything
```
nix-shell
# caution! if this is your first pull of first extension ever this might take some time
# depending on your network connection
# after it completes: inside the shell
make help
```

### Resources
- [Extension yaml docs](https://www.dynatrace.com/support/help/extend-dynatrace/extensions20/extension-yaml)
- [Extension knowledge base](https://www.dynatrace.com/support/help/extend-dynatrace/extensions20)

### Convinience
This section is entirely **optional**. The repository contains additional amenities, but they're not so straightforward, so we don't recommend them for begginers.  Anyway, you might also like:
- [`direnv`](https://direnv.net/) (which can be installed easily via `nix-env -iA nixpkgs.direnv`)

### Internal tooling
If you're a **Dynatrace employee** you can follow [this link](https://github.com/dynatrace-extensions/precious-toolz-internal) to enable internal tooling
