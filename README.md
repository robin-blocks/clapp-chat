# Chat Clapp

A ChatGPT/Manus-style chat interface for OpenClaw.

## Features

- **Responsive layout**: Sidebar on desktop, burger menu on mobile
- **Session management**: Create, switch, and delete conversations
- **Persistent history**: Sessions saved locally for reference
- **Markdown support**: Code blocks, formatting in messages
- **Auto-scroll**: Follows conversation as it flows

## Structure

```
chat/
├── clapp.json                # Manifest
├── views/
│   ├── chat.app.md           # App definition
│   └── default.chat.view.md  # Main view layout
├── components/
│   ├── ChatLayout.tsx        # Main responsive layout
│   ├── ChatMessages.tsx      # Message list with bubbles
│   └── ChatInput.tsx         # Input box with send
├── handlers/
│   └── chat-handler.ts       # Session & message management
└── README.md
```

## Usage

The chat clapp is installed by default. Access it from the clapps home screen.

### Keyboard shortcuts

- **Enter**: Send message
- **Shift+Enter**: New line

### Session storage

Sessions are stored in `~/.openclaw/workspace/chat-sessions/`:
- `_sessions.json` — Session metadata
- `session-<id>.json` — Messages for each session

## Intents

| Intent | Description |
|--------|-------------|
| `chat.init` | Load sessions and initialize state |
| `chat.send` | Send a message to the active session |
| `chat.newSession` | Create a new conversation |
| `chat.switchSession` | Switch to a different session |
| `chat.deleteSession` | Delete a session |

## Customization

To customize the chat interface:

1. Edit files in `~/.openclaw/clapps/chat/`
2. Changes take effect on reload
3. To contribute back, push changes and open a PR
