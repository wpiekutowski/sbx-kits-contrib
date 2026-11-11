## mise

[mise](https://mise.jdx.dev) is installed at `~/.local/bin/mise`. It manages the dev tools that the global config `~/.config/mise/config.toml` and each project's `mise.toml` declare.

- mise activates from `~/.bashrc`, which only interactive and login bash read. Elsewhere, including an agent's command shell, its tools are not on `PATH`: run them with `mise x -- <command>`, or through a task with `mise run <task>`.
- Inside `mise x` and mise tasks, a mise tool shadows a system tool of the same name.
- `[env]` in a `mise.toml` overrides variables already set in the shell.
- `MISE_TRUSTED_CONFIG_PATHS="/"` is exported from `~/.bashrc` only. If mise reports an untrusted config elsewhere, run `mise trust`.
- `mise ls` lists the installed tools and the config file that asks for each.
