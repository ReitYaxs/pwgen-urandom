# pwgen-urandom

*A minimalistic CLI utility for instant local password generation.*

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
The character set is intentionally restricted to symbols that are accepted by generally all websites.

**How to initiate**

Binary name: `noisepass`. Use this name to call the utility from the CLI.

**How to use**

`noisepass` → generates a 16 (by defualt) character password
`noisepass N` → generates a N character password

**Installation (user-level, no sudo):**

```
curl -fsSL https://raw.githubusercontent.com/hopsayer/pwgen-urandom/main/noisepass | install -m 755 /dev/stdin ~/.local/bin/noisepass
ln -sf ~/.local/bin/noisepass ~/.local/bin/pwgen-urandom    # Optional
```

**OR**

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


