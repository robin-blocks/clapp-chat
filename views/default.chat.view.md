---
name: chat
domain: default
version: 0.1.0
---

## State Bindings
- `chat.sessions` -> array
- `chat.activeSession` -> string
- `chat.messages` -> array
- `chat.loading` -> boolean

## Layout
```clapp-layout
ChatLayout():
```

## Intents
| Name | Payload | Description |
|------|---------|-------------|
| chat.init | `{}` | Initialize chat and load sessions |
| chat.send | `{ text: string, attachments?: Array<{ name: string, mimeType: string, size?: number, dataUrl: string }> }` | Send a message with optional pasted/uploaded images/files |
| chat.newSession | `{}` | Create a new chat session |
| chat.switchSession | `{ sessionKey: string }` | Switch to a different session |
| chat.deleteSession | `{ sessionKey: string }` | Delete a session |
| chat.loadOlder | `{}` | Load older messages for current session |
