# Kiro Autopilot Full Trust Config

## English

This repository provides a simple configuration for Kiro Autopilot / Kiro Agent that allows Kiro to run terminal commands without asking for confirmation every time. By adding `"*"` to `kiroAgent.trustedCommands`, you enable full auto-approve mode for terminal commands. This is useful if you want Kiro to work more autonomously and avoid constant permission prompts while coding. However, this mode should be used carefully, especially with unknown or untrusted projects, because Kiro will be able to run commands automatically. For better safety, this example also includes a denylist for dangerous commands.

```json
{
  "kiroAgent.trustedCommands": ["*"],
  "kiroAgent.commandDenylist": [
    "rm -rf",
    "sudo",
    "su ",
    "chmod 777",
    "chown *",
    "mkfs",
    "dd if=",
    "curl * | sh",
    "wget * | sh",
    "shutdown",
    "reboot"
  ]
}
```

## How to use

Open Kiro settings and add the configuration to your user `settings.json`.

You can open it through:

```text
Ctrl + Shift + P
```

Then search for:

```text
Preferences: Open User Settings (JSON)
```

After that, paste the configuration into the file and save it.

---

## Русский

Этот репозиторий содержит простой конфиг для Kiro Autopilot / Kiro Agent, который позволяет Kiro запускать команды в терминале без постоянного запроса подтверждения. Если добавить `"*"` в `kiroAgent.trustedCommands`, Kiro будет автоматически доверять всем командам терминала. Это удобно, если вы хотите, чтобы Kiro работал более автономно и не спрашивал разрешение на каждую команду во время разработки. Но использовать такой режим нужно осторожно, особенно в неизвестных или непроверенных проектах, потому что команды будут запускаться автоматически. Для большей безопасности в примере также добавлен denylist с опасными командами.

```json
{
  "kiroAgent.trustedCommands": ["*"],
  "kiroAgent.commandDenylist": [
    "rm -rf",
    "sudo",
    "su ",
    "chmod 777",
    "chown *",
    "mkfs",
    "dd if=",
    "curl * | sh",
    "wget * | sh",
    "shutdown",
    "reboot"
  ]
}
```

## Как использовать

Откройте настройки Kiro и добавьте конфиг в пользовательский файл `settings.json`.

Открыть его можно так:

```text
Ctrl + Shift + P
```

Затем найдите:

```text
Preferences: Open User Settings (JSON)
```

После этого вставьте конфиг в файл и сохраните его.
