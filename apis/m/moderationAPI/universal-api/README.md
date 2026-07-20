# <img src="https://images.mindcloud.co/apps/icons/favicon-docs-moderationapi-com-48x48_1778255425341.png" alt="Moderation API logo" width="28" height="28"> Moderation API: Universal API

Analyze and moderate text, images, audio, video, authors, review queues, moderation actions, and wordlists with the Moderation API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/moderationAPI/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 29
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://moderationapi.com
- **Vendor API docs:** https://docs.moderationapi.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Details](actions/get-account-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/get-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (29)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Details](actions/get-account-details.md) | GET | Retrieves account details from Moderation API. |

### Author

| Action | Method | Description |
| --- | --- | --- |
| [Create A New Author](actions/create-a-new-author.md) | POST | Creates a new author in Moderation API. |
| [Delete An Author](actions/delete-an-author.md) | DELETE | Deletes an author from Moderation API. |
| [Get Author Details](actions/get-author-details.md) | GET | Retrieves author details from Moderation API. |
| [List Authors](actions/list-authors.md) | GET | Retrieves authors from Moderation API. |
| [Update Author Details](actions/update-author-details.md) | PUT | Updates author details in Moderation API. |

### Moderation Action

| Action | Method | Description |
| --- | --- | --- |
| [Create An Action](actions/create-an-action.md) | POST | Creates a moderation action in Moderation API. |
| [Delete An Action](actions/delete-an-action.md) | DELETE | Deletes a moderation action from Moderation API. |
| [Execute Moderation Action](actions/execute-moderation-action.md) | POST | Executes a moderation action in Moderation API. |
| [Get An Action](actions/get-an-action.md) | GET | Retrieves a moderation action from Moderation API. |
| [List Moderation Actions](actions/list-moderation-actions.md) | GET | Retrieves moderation actions from Moderation API. |
| [Update An Action](actions/update-an-action.md) | PUT | Updates a moderation action in Moderation API. |

### Moderation Result

| Action | Method | Description |
| --- | --- | --- |
| [Analyze Audio](actions/analyze-audio.md) | POST | Submits audio to Moderation API for analysis. |
| [Analyze Image](actions/analyze-image.md) | POST | Submits an image to Moderation API for analysis. |
| [Analyze Object](actions/analyze-object.md) | POST | Submits an object to Moderation API for analysis. |
| [Analyze Text](actions/analyze-text.md) | POST | Submits text to Moderation API for analysis. |
| [Analyze Video](actions/analyze-video.md) | POST | Submits a video to Moderation API for analysis. |
| [Submit Content For Moderation](actions/submit-content-for-moderation.md) | POST | Submits content to Moderation API for moderation. |

### Queue Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Queue Items](actions/get-queue-items.md) | GET | Retrieves review queue items from Moderation API. |
| [Resolve A Queue Item](actions/resolve-a-queue-item.md) | PUT | Resolves a review queue item in Moderation API. |
| [Unresolve A Queue Item](actions/unresolve-a-queue-item.md) | PUT | Unresolves a review queue item in Moderation API. |

### Review Queue

| Action | Method | Description |
| --- | --- | --- |
| [Get A Queue](actions/get-a-queue.md) | GET | Retrieves a review queue from Moderation API. |
| [Get Queue Statistics](actions/get-queue-statistics.md) | GET | Retrieves review queue statistics from Moderation API. |

### Word

| Action | Method | Description |
| --- | --- | --- |
| [Add Words To Wordlist](actions/add-words-to-wordlist.md) | POST | Adds words to a wordlist in Moderation API. |
| [Remove Words From Wordlist](actions/remove-words-from-wordlist.md) | DELETE | Removes words from a wordlist in Moderation API. |

### Wordlist

| Action | Method | Description |
| --- | --- | --- |
| [Get Embedding Status](actions/get-embedding-status.md) | GET | Retrieves wordlist embedding status from Moderation API. |
| [Get Wordlist](actions/get-wordlist.md) | GET | Retrieves a wordlist from Moderation API. |
| [List Wordlists](actions/list-wordlists.md) | GET | Retrieves wordlists from Moderation API. |
| [Update Wordlist](actions/update-wordlist.md) | PUT | Updates a wordlist in Moderation API. |

