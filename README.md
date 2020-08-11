# `protect` a folder from accidental `rm -rf`

| Threat                        | Status            |
| ------                        | ------            |
| `rm -rf`                      | **Protected**     |
| `find . -delete`              | **Protected**     |
| `sudo rm -rf`                 | **NOT Protected** |
| `chmod -R 777 && rm -rf`      | **NOT Protected** |
| `dd if=/dev/zero of=/dev/sda` | **NOT Protected** |
| Gun shot into your disk       | **NOT Protected** |

## Install

```bash
# We recommand using https://github.com/b1f6c1c4/git-get
#     ... to download the script
# rua install git-get
git get -o ~/.local/bin/ b1f6c1c4/protect -- protect
```

## Dependency

- POSIX `sh`

## Usage

- To protect a folder against accidental `rm -rf`:

    ```bash
    protect <folder>...
    ```

- To stop protecting a folder:

    ```bash
    protect --disarm <folder>...
    ```
