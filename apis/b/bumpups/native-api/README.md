# Bumpups: Native API Reference

A consolidated summary of Bumpups's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.bumpups.com/docs/getting-started
- **API base URL:** `https://api.bumpups.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://docs.bumpups.com/docs/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Condition Assessment](actions/condition-assessment.md) | `POST /chat` | [docs](https://docs.bumpups.com/docs/prompt-cookbook/real-estate) |
| [Courtroom Proceedings Flowchart](actions/courtroom-proceedings-flowchart.md) | `POST /chat` | [docs](https://docs.bumpups.com/docs/prompt-cookbook/legal) |
| [Create Chat Response](actions/create-chat-response.md) | `POST /chat` | [docs](https://docs.bumpups.com/api-reference) |
| [Deposition Follow-Up Questions](actions/deposition-follow-up-questions.md) | `POST /chat` | [docs](https://docs.bumpups.com/docs/prompt-cookbook/legal) |
| [Deposition Issue Identification](actions/deposition-issue-identification.md) | `POST /chat` | [docs](https://docs.bumpups.com/docs/prompt-cookbook/legal) |
| [Deposition Summary](actions/deposition-summary.md) | `POST /chat` | [docs](https://docs.bumpups.com/docs/prompt-cookbook/legal) |
| [Generate Hashtags](actions/generate-hashtags.md) | `POST /creator/hashtags` | [docs](https://docs.bumpups.com/api-reference) |
| [Generate Key Takeaways](actions/generate-key-takeaways.md) | `POST /creator/takeaways` | [docs](https://docs.bumpups.com/api-reference) |
| [Generate Keywords](actions/generate-keywords.md) | `POST /creator/hashtags` | [docs](https://docs.bumpups.com/api-reference) |
| [Generate Timestamps](actions/generate-timestamps.md) | `POST /general/timestamps` | [docs](https://docs.bumpups.com/api-reference) |
| [Generate Titles](actions/generate-titles.md) | `POST /creator/titles` | [docs](https://docs.bumpups.com/api-reference) |
| [Generate Video Description](actions/generate-video-description.md) | `POST /creator/description` | [docs](https://docs.bumpups.com/api-reference) |
| [Highlight Moments](actions/highlight-moments.md) | `POST /chat` | [docs](https://docs.bumpups.com/docs/prompt-cookbook/content-editor) |
| [LinkedIn Post from Video](actions/linked-in-post-from-video.md) | `POST /chat` | [docs](https://docs.bumpups.com/docs/prompt-cookbook/content-creator) |
| [Newsletter Intro from Video](actions/newsletter-intro-from-video.md) | `POST /chat` | [docs](https://docs.bumpups.com/docs/prompt-cookbook/content-creator) |
| [Pacing Analysis](actions/pacing-analysis.md) | `POST /chat` | [docs](https://docs.bumpups.com/docs/prompt-cookbook/content-editor) |
| [Paid Ad Copy from Video](actions/paid-ad-copy-from-video.md) | `POST /chat` | [docs](https://docs.bumpups.com/docs/prompt-cookbook/content-creator) |
| [Property Features Summary](actions/property-features-summary.md) | `POST /chat` | [docs](https://docs.bumpups.com/docs/prompt-cookbook/real-estate) |
| [Property Layout Analysis](actions/property-layout-analysis.md) | `POST /chat` | [docs](https://docs.bumpups.com/docs/prompt-cookbook/real-estate) |
| [Social Thread from Video](actions/social-thread-from-video.md) | `POST /chat` | [docs](https://docs.bumpups.com/docs/prompt-cookbook/content-creator) |
| [Staging Recommendations](actions/staging-recommendations.md) | `POST /chat` | [docs](https://docs.bumpups.com/docs/prompt-cookbook/real-estate) |
| [Student Flashcards](actions/student-flashcards.md) | `POST /chat` | [docs](https://docs.bumpups.com/docs/prompt-cookbook/student) |
| [Student Mixed Quiz](actions/student-mixed-quiz.md) | `POST /chat` | [docs](https://docs.bumpups.com/docs/prompt-cookbook/student) |
| [Student Real-World Application](actions/student-real-world-application.md) | `POST /chat` | [docs](https://docs.bumpups.com/docs/prompt-cookbook/student) |
| [Student Study Guide Outline](actions/student-study-guide-outline.md) | `POST /chat` | [docs](https://docs.bumpups.com/docs/prompt-cookbook/student) |
| [Summarize Video](actions/summarize-video.md) | `POST /chat` | [docs](https://docs.bumpups.com/api-reference) |
| [Teacher Discussion Prompts](actions/teacher-discussion-prompts.md) | `POST /chat` | [docs](https://docs.bumpups.com/docs/prompt-cookbook/teacher) |
| [Teacher Lesson Plan](actions/teacher-lesson-plan.md) | `POST /chat` | [docs](https://docs.bumpups.com/docs/prompt-cookbook/teacher) |
| [Teacher Standards Alignment](actions/teacher-standards-alignment.md) | `POST /chat` | [docs](https://docs.bumpups.com/docs/prompt-cookbook/teacher) |
| [Teacher Tiered Activities](actions/teacher-tiered-activities.md) | `POST /chat` | [docs](https://docs.bumpups.com/docs/prompt-cookbook/teacher) |
