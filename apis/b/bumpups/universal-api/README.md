# <img src="https://images.mindcloud.co/apps/icons/bumpups_1775764308572.png" alt="Bumpups logo" width="28" height="28"> Bumpups: Universal API

Analyze videos and generate summaries, timestamps, and prompt-based content

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bumpups/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://bumpups.com
- **Vendor API docs:** https://docs.bumpups.com/docs/getting-started

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Condition Assessment](actions/condition-assessment.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bumpups/latest/actions/condition-assessment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

## Actions (30)

### Content Creator

| Action | Method | Description |
| --- | --- | --- |
| [LinkedIn Post from Video](actions/linked-in-post-from-video.md) | POST | Creates a LinkedIn post from a video in Bumpups. |
| [Newsletter Intro from Video](actions/newsletter-intro-from-video.md) | POST | Creates a newsletter intro from a video in Bumpups. |
| [Paid Ad Copy from Video](actions/paid-ad-copy-from-video.md) | POST | Creates paid ad copy from a video in Bumpups. |
| [Social Thread from Video](actions/social-thread-from-video.md) | POST | Creates a social thread from a video in Bumpups. |

### Content Editor

| Action | Method | Description |
| --- | --- | --- |
| [Highlight Moments](actions/highlight-moments.md) | POST | Creates highlight moments from a video in Bumpups. |
| [Pacing Analysis](actions/pacing-analysis.md) | POST | Creates a pacing analysis from a video in Bumpups. |

### Core

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Response](actions/create-chat-response.md) | POST | Creates a chat response from a video in Bumpups. |
| [Generate Hashtags](actions/generate-hashtags.md) | POST | Creates hashtags for a video in Bumpups. |
| [Generate Key Takeaways](actions/generate-key-takeaways.md) | POST | Creates key takeaways from a video in Bumpups. |
| [Generate Keywords](actions/generate-keywords.md) | POST | Creates keywords for a video in Bumpups. |
| [Generate Timestamps](actions/generate-timestamps.md) | POST | Creates timestamps for a video in Bumpups. |
| [Generate Titles](actions/generate-titles.md) | POST | Creates title suggestions for a video in Bumpups. |
| [Generate Video Description](actions/generate-video-description.md) | POST | Creates a video description in Bumpups. |
| [Summarize Video](actions/summarize-video.md) | POST | Creates a video summary in Bumpups. |

### Legal

| Action | Method | Description |
| --- | --- | --- |
| [Courtroom Proceedings Flowchart](actions/courtroom-proceedings-flowchart.md) | POST | Creates a courtroom proceedings flowchart in Bumpups. |
| [Deposition Follow-Up Questions](actions/deposition-follow-up-questions.md) | POST | Creates deposition follow-up questions in Bumpups. |
| [Deposition Issue Identification](actions/deposition-issue-identification.md) | POST | Creates legal issue identification from a video in Bumpups. |
| [Deposition Summary](actions/deposition-summary.md) | POST | Creates a deposition summary from a video in Bumpups. |

### Real Estate

| Action | Method | Description |
| --- | --- | --- |
| [Condition Assessment](actions/condition-assessment.md) | POST | Creates a condition assessment from a video in Bumpups. |
| [Property Features Summary](actions/property-features-summary.md) | POST | Creates a property features summary from a video in Bumpups. |
| [Property Layout Analysis](actions/property-layout-analysis.md) | POST | Creates a property layout analysis from a video in Bumpups. |
| [Staging Recommendations](actions/staging-recommendations.md) | POST | Creates staging recommendations from a video in Bumpups. |

### Student

| Action | Method | Description |
| --- | --- | --- |
| [Student Flashcards](actions/student-flashcards.md) | POST | Creates flashcards from a video in Bumpups. |
| [Student Mixed Quiz](actions/student-mixed-quiz.md) | POST | Creates a mixed quiz from a video in Bumpups. |
| [Student Real-World Application](actions/student-real-world-application.md) | POST | Creates real-world application ideas from a video in Bumpups. |
| [Student Study Guide Outline](actions/student-study-guide-outline.md) | POST | Creates a study guide outline from a video in Bumpups. |

### Teacher

| Action | Method | Description |
| --- | --- | --- |
| [Teacher Discussion Prompts](actions/teacher-discussion-prompts.md) | POST | Creates discussion prompts from a video in Bumpups. |
| [Teacher Lesson Plan](actions/teacher-lesson-plan.md) | POST | Creates a teacher lesson plan from a video in Bumpups. |
| [Teacher Standards Alignment](actions/teacher-standards-alignment.md) | POST | Creates standards alignment from a video in Bumpups. |
| [Teacher Tiered Activities](actions/teacher-tiered-activities.md) | POST | Creates tiered learning activities from a video in Bumpups. |

