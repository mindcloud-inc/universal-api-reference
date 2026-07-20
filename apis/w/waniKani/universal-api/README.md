# <img src="https://images.mindcloud.co/apps/icons/wani-kani_1775491420588.png" alt="WaniKani logo" width="28" height="28"> WaniKani: Universal API

Learn Japanese kanji, vocabulary, and track progress

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/waniKani/latest
- **Category:** Human Resources / Learning (LMS)
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.wanikani.com
- **Vendor API docs:** https://docs.api.wanikani.com/20170710/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Information](actions/get-user-information.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waniKani/latest/actions/get-user-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Level Progression

| Action | Method | Description |
| --- | --- | --- |
| [Get Level Progression](actions/get-level-progression.md) | GET | Retrieves a level progression from WaniKani. |
| [List Level Progressions](actions/list-level-progressions.md) | GET | Retrieves level progressions from WaniKani. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create Study Material](actions/create-study-material.md) | POST | Creates a new study material in WaniKani. |
| [Get Assignment](actions/get-assignment.md) | GET | Retrieves an assignment from WaniKani. |
| [Get Review Statistic](actions/get-review-statistic.md) | GET | Retrieves a review statistic from WaniKani. |
| [Get Study Material](actions/get-study-material.md) | GET | Retrieves a study material from WaniKani. |
| [List Assignments](actions/list-assignments.md) | GET | Retrieves assignments from WaniKani. |
| [List Review Statistics](actions/list-review-statistics.md) | GET | Retrieves review statistics from WaniKani. |
| [List Study Materials](actions/list-study-materials.md) | GET | Retrieves study materials from WaniKani. |
| [Start Assignment](actions/start-assignment.md) | PUT | Starts an assignment in WaniKani. |
| [Update Study Material](actions/update-study-material.md) | PUT | Updates an existing study material in WaniKani. |

### Reset

| Action | Method | Description |
| --- | --- | --- |
| [List Resets](actions/list-resets.md) | GET | Retrieves resets from WaniKani. |

### Spaced Repetition System

| Action | Method | Description |
| --- | --- | --- |
| [Get Spaced Repetition System](actions/get-spaced-repetition-system.md) | GET | Retrieves a spaced repetition system from WaniKani. |
| [List Spaced Repetition Systems](actions/list-spaced-repetition-systems.md) | GET | Retrieves spaced repetition systems from WaniKani. |

### Subject

| Action | Method | Description |
| --- | --- | --- |
| [Get Subject](actions/get-subject.md) | GET | Retrieves a subject from WaniKani. |
| [List Subjects](actions/list-subjects.md) | GET | Retrieves subjects from WaniKani. |

### Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Summary](actions/get-summary.md) | GET | Retrieves a summary from WaniKani. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User Information](actions/get-user-information.md) | GET | Retrieves user information from WaniKani. |
| [Update User Information](actions/update-user-information.md) | PUT | Updates user information in WaniKani. |

### Voice Actor

| Action | Method | Description |
| --- | --- | --- |
| [Get Voice Actor](actions/get-voice-actor.md) | GET | Retrieves a voice actor from WaniKani. |
| [List Voice Actors](actions/list-voice-actors.md) | GET | Retrieves voice actors from WaniKani. |

