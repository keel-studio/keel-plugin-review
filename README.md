# keel plugin: Code Review

Review GitHub and GitLab pull requests inside the Code page. AI comments wait for your OK before they are posted.

> **Status: planned.** The code still lives in [keel-v2](https://github.com/MiladNalbandi/keel-v2). It moves here step by step, as
> [the plugin plan](https://github.com/MiladNalbandi/keel-v2/tree/main/docs/plugins) says. There is nothing to install yet.

| | |
| --- | --- |
| id | `review` |
| needs | keel core (plugin SDK 1), Code |
| works with | KeelBot |
| parts | api · web · content · migrations |
| trust level | runs code in keel |

**What it adds to keel**

- Code › Review
- GitLab connection
- KeelBot commands /review-branch, /explain-pr

**Where the code is today (keel-v2)**

- `keel.api.review` (api)
- `web/src/components/review/*`
- `web/src/reviewApi.ts`
- `content/plugins/review`

## Layout

```
keel-plugin.yml   the manifest
api/              Kotlin, a thin Spring Boot jar
web/              React pages and slots (an ES module)
content/          workflows, agents, skills, commands
migrations/       its own database tables (own Flyway history)
```

## Install

When it is released: in keel, **Control › Plugins › Marketplace › Code Review › Install**. keel checks the file's
signature, shows what the plugin may do, and asks you before it installs.

## License

MIT
