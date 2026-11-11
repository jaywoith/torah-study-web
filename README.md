# Torah Study Web Client

Web client for the multi-platform Torah independent study app.

## Role

- Pure consumer of the [torah-study-backend](https://github.com/jaywoith/torah-study-backend) API
- Renders daily study, Siddur path, Musar/Kabbalah paths, and AI Rabbi Coach
- Contains **no** framework logic, generation rules, or AI prompts

## Related Repositories

| Repo | Purpose |
|------|---------|
| [torah-study-shared](https://github.com/jaywoith/torah-study-shared) | Shared packages (source of truth) |
| [torah-study-backend](https://github.com/jaywoith/torah-study-backend) | Backend API (this client talks only to it) |
| [torah-study-ios](https://github.com/jaywoith/torah-study-ios) | iOS client |
| [torah-study-android](https://github.com/jaywoith/torah-study-android) | Android client |

## Drift Prevention

This client never imports shared packages. It only calls backend endpoints and renders the JSON it receives. Any change to study content or AI behavior happens in the shared packages + backend; the web client only needs to adapt if the public API shape changes.

## Next Steps

- Scaffold Next.js / React app
- Implement profile selection (framework, level, interests, language mode)
- Render daily study units and Siddur path
- Chat UI for AI Rabbi Coach
