# pwgen-urandom — minimalistic command-line password generator.

Supports GNU/Linux, NixOS and macOS (including Homebrew setups).

**What it does**

Generates a random password of a given length using characters from:
A–Z a–z 0–9 and a conservative set of special symbols:
`A-Za-z0-9!@#$%^*()-_+[]{}~`

**Example:**

```
$ noisepass
NGEGCHmLsyk#ZUuQ
```

**How it works**

Uses `/dev/urandom` as the entropy source.
The character set is intentionally restricted to symbols that are commonly accepted by various websites.

**Usage**

Binary name: `noisepass`. Use this name to call the utility from the CLI.

`noisepass` → generates a 16 (by default) character password

`noisepass N` → generates an N character password

**Installation (user-level, no sudo):**

```
curl -fsSL https://raw.githubusercontent.com/hopsayer/pwgen-urandom/main/noisepass | install -m 755 /dev/stdin ~/.local/bin/noisepass
ln -sf ~/.local/bin/noisepass ~/.local/bin/pwgen-urandom    # Optional
```

**Or alternatively:**

```
git clone https://github.com/hopsayer/pwgen-urandom.git
cd pwgen-urandom
install -m 755 noisepass ~/.local/bin/noisepass
ln -sf ~/.local/bin/noisepass ~/.local/bin/pwgen-urandom    # Optional
```

**Requirements (very basic):**

- `bash`
- coreutils (`tr`, `head`)
- `/dev/urandom`


