# Linux Notes

Commands I learned and used in my Kali Linux lab, with the reason I use each one.

## Navigating and reading
- `ls`, `ls -a`: list files, including hidden ones (names starting with a dot)
- `cd`, `pwd`: move between folders and show where I am
- `cat`: print a file. Files with odd names need `./name` or quotes
- `man`: read a command's manual (`/word` searches, `q` quits)

## Searching
- `find`: search by conditions (size, owner, group, type) instead of checking files by hand
- `grep`: print only the lines containing a word
- `strings`: pull readable text out of a binary file
- `file`: identify a file's real type before opening it

## Processing text
- `sort` and `uniq`: sort first, because uniq only compares neighbouring lines
- `diff`: show only the lines that differ between two files
- `tr`: translate characters one-for-one
- `|` (pipe): feed one command's output into the next
- `>` and `>>`: save output to a file (`>` overwrites, `>>` appends)

## Encoding and compression
- `base64` / `base64 -d`: encoding, not encryption, since anyone can reverse it
- `xxd -r`: turn a hexdump back into a file
- `gzip`, `bzip2`, `tar`: compression layers, always checked with `file` first

## Networking and remote access
- `ssh`: log in to another machine, or run one command on it
- `scp`: copy files over SSH (the port flag is a capital `-P`)
- `nc`: send text to a port
- `openssl s_client`: talk to a port that uses TLS
- `nmap`: scan ports and detect services (`-sV` for versions)
- SSH keys: private keys must be `chmod 600` and never shared

## Habits
- Check `ls` and `file` before guessing
- Look at the prompt to see which machine I am on
- Keep a log: one line per session
