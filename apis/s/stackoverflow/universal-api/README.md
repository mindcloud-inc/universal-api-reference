# <img src="https://images.mindcloud.co/apps/icons/stackoverflow_1776343195839.png" alt="Stackoverflow logo" width="28" height="28"> Stackoverflow: Universal API

Access Stack Exchange network data and moderation-safe write operations across Stack Overflow and other Stack Exchange sites.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/stackoverflow/latest
- **Actions:** 143
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://stackoverflow.com
- **Vendor API docs:** https://api.stackexchange.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Authenticated User](actions/get-authenticated-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID&site=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (143)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Deauthenticate Access Tokens](actions/deauthenticate-access-tokens.md) | GET | Deauthenticates application access tokens in Stackoverflow. |
| [Invalidate Access Tokens](actions/invalidate-access-tokens.md) | GET | Invalidates existing access tokens in Stackoverflow. |
| [Read Access Tokens](actions/read-access-tokens.md) | GET | Retrieves specific access token details from Stackoverflow. |

### Achievement

| Action | Method | Description |
| --- | --- | --- |
| [List User Achievements](actions/list-user-achievements.md) | GET | Retrieves a user's achievements from Stackoverflow. |

### Answer

| Action | Method | Description |
| --- | --- | --- |
| [Accept Answer](actions/accept-answer.md) | PUT | Accepts an existing answer in Stackoverflow. |
| [Create Answer](actions/create-answer.md) | POST | Creates a new answer in Stackoverflow. |
| [Create Answer Flag](actions/create-answer-flag.md) | POST | Creates a flag for an answer in Stackoverflow. |
| [Delete Answer](actions/delete-answer.md) | DELETE | Deletes an existing answer from Stackoverflow. |
| [Downvote Answer](actions/downvote-answer.md) | PUT | Adds a downvote to an answer in Stackoverflow. |
| [Edit Answer](actions/edit-answer.md) | PUT | Updates an existing answer in Stackoverflow. |
| [Get Answers](actions/get-answers.md) | GET | Retrieves specific answers from Stackoverflow. |
| [List Answers](actions/list-answers.md) | GET | Retrieves answers from Stackoverflow. |
| [List Collective Answers](actions/list-collective-answers.md) | GET | Retrieves answers for collectives from Stackoverflow. |
| [List Question Answers](actions/list-question-answers.md) | GET | Retrieves answers for questions from Stackoverflow. |
| [List User Answers](actions/list-user-answers.md) | GET | Retrieves answers for specific users from Stackoverflow. |
| [Recommend Answer](actions/recommend-answer.md) | PUT | Recommends an existing answer in Stackoverflow. |
| [List Top Answers In Tags By User](actions/top-user-answers-in-tags.md) | GET | Retrieves a user's top answers in tags from Stackoverflow. |
| [Undo Answer Acceptance](actions/undo-accept-answer.md) | PUT | Removes acceptance from an answer in Stackoverflow. |
| [Undo Answer Downvote](actions/undo-downvote-answer.md) | PUT | Removes a downvote from an answer in Stackoverflow. |
| [Undo Answer Recommendation](actions/undo-recommend-answer.md) | PUT | Removes an answer recommendation in Stackoverflow. |
| [Undo Answer Upvote](actions/undo-upvote-answer.md) | PUT | Removes an upvote from an answer in Stackoverflow. |
| [Upvote Answer](actions/upvote-answer.md) | PUT | Adds an upvote to an answer in Stackoverflow. |

### Badge

| Action | Method | Description |
| --- | --- | --- |
| [Get Badges](actions/get-badges.md) | GET | Retrieves specific badges from Stackoverflow. |
| [List Badge Recipients](actions/list-badge-recipients.md) | GET | Retrieves badge recipients from Stackoverflow. |
| [List Badge Recipients By Badge](actions/list-badge-recipients-by-badge.md) | GET | Retrieves badge recipients for specific badges from Stackoverflow. |
| [List Badges](actions/list-badges.md) | GET | Retrieves badges from Stackoverflow. |
| [List Badges By Name](actions/list-badges-by-name.md) | GET | Retrieves badges by name from Stackoverflow. |
| [List Badges By Tag](actions/list-badges-by-tag.md) | GET | Retrieves badges by tag from Stackoverflow. |
| [List User Badges](actions/list-user-badges.md) | GET | Retrieves badges for specific users from Stackoverflow. |

### Close Option

| Action | Method | Description |
| --- | --- | --- |
| [List Question Close Options](actions/question-close-options.md) | GET | Retrieves question close options from Stackoverflow. |

### Collective

| Action | Method | Description |
| --- | --- | --- |
| [Get Collectives](actions/get-collectives.md) | GET | Retrieves specific collectives from Stackoverflow. |
| [List Collectives](actions/list-collectives.md) | GET | Retrieves collectives from Stackoverflow. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | POST | Creates a new comment in Stackoverflow. |
| [Create Comment Flag](actions/create-comment-flag.md) | POST | Creates a flag for a comment in Stackoverflow. |
| [Delete Comment](actions/delete-comment.md) | DELETE | Deletes an existing comment from Stackoverflow. |
| [Edit Comment](actions/edit-comment.md) | PUT | Updates an existing comment in Stackoverflow. |
| [Get Comments](actions/get-comments.md) | GET | Retrieves specific comments from Stackoverflow. |
| [List Answer Comments](actions/list-answer-comments.md) | GET | Retrieves comments for answers from Stackoverflow. |
| [List Comments](actions/list-comments.md) | GET | Retrieves comments from Stackoverflow. |
| [List Comments By User To User](actions/list-comments-by-user-to-user.md) | GET | Retrieves comments from one user to another from Stackoverflow. |
| [List Post Comments](actions/list-post-comments.md) | GET | Retrieves comments for posts from Stackoverflow. |
| [List Question Comments](actions/list-question-comments.md) | GET | Retrieves comments for questions from Stackoverflow. |
| [List User Comments](actions/list-user-comments.md) | GET | Retrieves comments for specific users from Stackoverflow. |
| [List Mentioned Comments](actions/mentions-on-users.md) | GET | Retrieves comments that mention users from Stackoverflow. |
| [Undo Comment Upvote](actions/undo-upvote-comment.md) | PUT | Removes an upvote from a comment in Stackoverflow. |
| [Upvote Comment](actions/upvote-comment.md) | PUT | Adds an upvote to a comment in Stackoverflow. |

### Error

| Action | Method | Description |
| --- | --- | --- |
| [Get Error Definition](actions/get-error-definition.md) | GET | Retrieves an API error definition from Stackoverflow. |
| [List Errors](actions/list-errors.md) | GET | Retrieves API error definitions from Stackoverflow. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [List Events](actions/events.md) | GET | Retrieves recent events from Stackoverflow. |

### Filter

| Action | Method | Description |
| --- | --- | --- |
| [Create Filter](actions/create-filter.md) | GET | Creates a custom filter in Stackoverflow. |
| [Read Filter](actions/read-filter.md) | GET | Retrieves specific filter details from Stackoverflow. |

### Flag Option

| Action | Method | Description |
| --- | --- | --- |
| [List Answer Flag Options](actions/list-answer-flag-options.md) | GET | Retrieves answer flag options from Stackoverflow. |
| [List Comment Flag Options](actions/list-comment-flag-options.md) | GET | Retrieves comment flag options from Stackoverflow. |
| [List Question Flag Options](actions/question-flag-options.md) | GET | Retrieves question flag options from Stackoverflow. |

### Inbox Item

| Action | Method | Description |
| --- | --- | --- |
| [List Inbox Items](actions/inbox.md) | GET | Retrieves inbox items from Stackoverflow. |
| [List Unread Inbox Items](actions/inbox-unread.md) | GET | Retrieves unread inbox items from Stackoverflow. |
| [List User Inbox](actions/user-inbox.md) | GET | Retrieves a user's inbox from Stackoverflow. |
| [List User Unread Inbox](actions/user-unread-inbox.md) | GET | Retrieves a user's unread inbox items from Stackoverflow. |

### Info

| Action | Method | Description |
| --- | --- | --- |
| [Get Site Info](actions/get-site-info.md) | GET | Retrieves specific site information from Stackoverflow. |

### Merge Event

| Action | Method | Description |
| --- | --- | --- |
| [List Merge History](actions/merge-history.md) | GET | Retrieves user account merge history from Stackoverflow. |

### Network Activity

| Action | Method | Description |
| --- | --- | --- |
| [List User Network Activity](actions/users-network-activity.md) | GET | Retrieves a user's network activity from Stackoverflow. |

### Notification

| Action | Method | Description |
| --- | --- | --- |
| [List Notifications](actions/notifications.md) | GET | Retrieves notifications from Stackoverflow. |
| [List Unread Notifications](actions/unread-notifications.md) | GET | Retrieves unread notifications from Stackoverflow. |
| [List User Notifications](actions/user-notifications.md) | GET | Retrieves a user's notifications from Stackoverflow. |
| [List User Unread Notifications](actions/user-unread-notifications.md) | GET | Retrieves a user's unread notifications from Stackoverflow. |

### Post

| Action | Method | Description |
| --- | --- | --- |
| [Get Posts](actions/get-posts.md) | GET | Retrieves specific posts from Stackoverflow. |
| [List Posts](actions/list-posts.md) | GET | Retrieves posts from Stackoverflow. |
| [List Posts By User](actions/posts-on-users.md) | GET | Retrieves posts for specific users from Stackoverflow. |

### Privilege

| Action | Method | Description |
| --- | --- | --- |
| [List Privileges](actions/list-privileges.md) | GET | Retrieves site privileges from Stackoverflow. |
| [List User Privileges](actions/privileges-on-users.md) | GET | Retrieves a user's privileges from Stackoverflow. |

### Question

| Action | Method | Description |
| --- | --- | --- |
| [Advanced Search Questions](actions/advanced-search-questions.md) | GET | Finds questions in Stackoverflow with advanced search. |
| [Create Question](actions/create-question.md) | POST | Creates a new question in Stackoverflow. |
| [Create Question Flag](actions/create-question-flag.md) | POST | Creates a flag for a question in Stackoverflow. |
| [Delete Question](actions/delete-question.md) | DELETE | Deletes an existing question from Stackoverflow. |
| [Downvote Question](actions/downvote-question.md) | PUT | Adds a downvote to a question in Stackoverflow. |
| [Edit Question](actions/edit-question.md) | PUT | Updates an existing question in Stackoverflow. |
| [Favorite Question](actions/favorite-question.md) | PUT | Adds a question to favorites in Stackoverflow. |
| [List Featured Questions By User](actions/featured-questions-on-users.md) | GET | Retrieves featured questions for specific users from Stackoverflow. |
| [Get Questions](actions/get-questions.md) | GET | Retrieves specific questions from Stackoverflow. |
| [List Featured Questions](actions/list-featured-questions.md) | GET | Retrieves featured questions from Stackoverflow. |
| [List Linked Questions](actions/list-linked-questions.md) | GET | Retrieves linked questions from Stackoverflow. |
| [List Questions](actions/list-questions.md) | GET | Retrieves questions from Stackoverflow. |
| [List Related Questions](actions/list-related-questions.md) | GET | Retrieves related questions from Stackoverflow. |
| [List Tag FAQs](actions/list-tag-faqs.md) | GET | Retrieves tag FAQs from Stackoverflow. |
| [List Unanswered Questions](actions/list-unanswered-questions.md) | GET | Retrieves questions without answers from Stackoverflow. |
| [List User Favorites](actions/list-user-favorites.md) | GET | Retrieves favorite questions for specific users from Stackoverflow. |
| [List User Questions](actions/list-user-questions.md) | GET | Retrieves questions for specific users from Stackoverflow. |
| [List No-Answer Questions By User](actions/no-answer-questions-on-users.md) | GET | Retrieves questions without answers for specific users from Stackoverflow. |
| [List Questions By Answer](actions/questions-by-answer-ids.md) | GET | Retrieves questions for specific answers from Stackoverflow. |
| [List Collective Questions](actions/questions-by-collective.md) | GET | Retrieves questions for collectives from Stackoverflow. |
| [Search Questions](actions/search-questions.md) | GET | Finds questions in Stackoverflow by search query. |
| [Find Similar Questions](actions/similar.md) | GET | Finds similar questions in Stackoverflow. |
| [List Top Questions In Tags By User](actions/top-user-questions-in-tags.md) | GET | Retrieves a user's top questions in tags from Stackoverflow. |
| [List Unaccepted Questions By User](actions/unaccepted-questions-on-users.md) | GET | Retrieves unaccepted questions for specific users from Stackoverflow. |
| [List Unanswered Questions](actions/unanswered-questions.md) | GET | Retrieves unanswered questions from Stackoverflow. |
| [List Unanswered Questions In My Tags](actions/unanswered-questions-my-tags.md) | GET | Retrieves unanswered questions in your tags from Stackoverflow. |
| [List Unanswered Questions By User](actions/unanswered-questions-on-users.md) | GET | Retrieves unanswered questions for specific users from Stackoverflow. |
| [Undo Question Downvote](actions/undo-downvote-question.md) | PUT | Removes a downvote from a question in Stackoverflow. |
| [Undo Favorite Question](actions/undo-favorite-question.md) | PUT | Removes a question from favorites in Stackoverflow. |
| [Undo Question Upvote](actions/undo-upvote-question.md) | PUT | Removes an upvote from a question in Stackoverflow. |
| [Upvote Question](actions/upvote-question.md) | PUT | Adds an upvote to a question in Stackoverflow. |

### Question Timeline

| Action | Method | Description |
| --- | --- | --- |
| [List Question Timeline](actions/list-question-timeline.md) | GET | Retrieves question timeline entries from Stackoverflow. |

### Rendered Answer

| Action | Method | Description |
| --- | --- | --- |
| [Render Answer](actions/render-answer.md) | POST | Renders an answer preview in Stackoverflow. |

### Rendered Comment

| Action | Method | Description |
| --- | --- | --- |
| [Render Comment](actions/render-comment.md) | POST | Renders a comment preview in Stackoverflow. |

### Rendered Question

| Action | Method | Description |
| --- | --- | --- |
| [Render Question](actions/render-question.md) | POST | Renders a question preview in Stackoverflow. |

### Reputation

| Action | Method | Description |
| --- | --- | --- |
| [List User Reputation](actions/list-user-reputation.md) | GET | Retrieves reputation changes for specific users from Stackoverflow. |

### Reputation History

| Action | Method | Description |
| --- | --- | --- |
| [List Full Reputation History](actions/full-reputation-history.md) | GET | Retrieves a user's full reputation history from Stackoverflow. |
| [List User Reputation History](actions/list-user-reputation-history.md) | GET | Retrieves reputation history for specific users from Stackoverflow. |

### Revision

| Action | Method | Description |
| --- | --- | --- |
| [List Revisions By GUID](actions/revisions-by-guids.md) | GET | Retrieves revisions by GUID from Stackoverflow. |
| [List Revisions By Post](actions/revisions-by-ids.md) | GET | Retrieves revisions for specific posts from Stackoverflow. |

### Search Excerpt

| Action | Method | Description |
| --- | --- | --- |
| [Search Question Excerpts](actions/search-question-excerpts.md) | GET | Finds question excerpts in Stackoverflow by search query. |

### Site

| Action | Method | Description |
| --- | --- | --- |
| [List Sites](actions/list-sites.md) | GET | Retrieves Stack Exchange sites from Stackoverflow. |

### Suggested Edit

| Action | Method | Description |
| --- | --- | --- |
| [Create Answer Suggested Edit](actions/create-answer-suggested-edit.md) | POST | Creates a suggested edit for an answer in Stackoverflow. |
| [Create Question Suggested Edit](actions/create-question-suggested-edit.md) | POST | Creates a suggested edit for a question in Stackoverflow. |
| [List Suggested Edits On Posts](actions/posts-on-suggested-edits.md) | GET | Retrieves suggested edits for specific posts from Stackoverflow. |
| [List Suggested Edits](actions/suggested-edits.md) | GET | Retrieves suggested edits from Stackoverflow. |
| [Get Suggested Edits](actions/suggested-edits-by-ids.md) | GET | Retrieves specific suggested edits from Stackoverflow. |
| [List Suggested Edits By User](actions/suggested-edits-on-users.md) | GET | Retrieves suggested edits for specific users from Stackoverflow. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Get Tag Info](actions/get-tag-info.md) | GET | Retrieves specific tag information from Stackoverflow. |
| [List Related Tags](actions/list-related-tags.md) | GET | Retrieves related tags from Stackoverflow. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from Stackoverflow. |
| [List Moderator-Only Tags](actions/moderator-only-tags.md) | GET | Retrieves moderator-only tags from Stackoverflow. |
| [List Required Tags](actions/required-tags.md) | GET | Retrieves required tags from Stackoverflow. |
| [List Collective Tags](actions/tags-by-collective.md) | GET | Retrieves tags for collectives from Stackoverflow. |
| [List User Tags](actions/tags-on-users.md) | GET | Retrieves tags for specific users from Stackoverflow. |

### Tag Preference

| Action | Method | Description |
| --- | --- | --- |
| [Edit Tag Preferences](actions/edit-tag-prefs-on-user.md) | PUT | Updates a user's tag preferences in Stackoverflow. |
| [List Tag Preferences](actions/tag-prefs-on-user.md) | GET | Retrieves a user's tag preferences from Stackoverflow. |

### Tag Score

| Action | Method | Description |
| --- | --- | --- |
| [List Top Answerers For Tag](actions/list-top-answerers-for-tag.md) | GET | Retrieves top answerers for a tag from Stackoverflow. |
| [List Top Askers For Tag](actions/list-top-askers-for-tag.md) | GET | Retrieves top askers for a tag from Stackoverflow. |

### Tag Synonym

| Action | Method | Description |
| --- | --- | --- |
| [List Tag Synonyms](actions/list-tag-synonyms.md) | GET | Retrieves tag synonyms for specific tags from Stackoverflow. |
| [List Tag Synonyms](actions/tag-synonyms.md) | GET | Retrieves tag synonyms from Stackoverflow. |

### Tag Wiki

| Action | Method | Description |
| --- | --- | --- |
| [List Tag Wikis](actions/wikis-by-tags.md) | GET | Retrieves tag wikis from Stackoverflow. |

### Top Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Top Answer Tags By User](actions/top-answer-tags-on-users.md) | GET | Retrieves a user's top answer tags from Stackoverflow. |
| [List Top Question Tags By User](actions/top-question-tags-on-users.md) | GET | Retrieves a user's top question tags from Stackoverflow. |
| [List Top Tags By User](actions/top-tags-on-users.md) | GET | Retrieves a user's top tags from Stackoverflow. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Authenticated User](actions/get-authenticated-user.md) | GET | Retrieves the authenticated user from Stackoverflow. |
| [Get Users](actions/get-users.md) | GET | Retrieves specific users from Stackoverflow. |
| [List Associated Users](actions/list-associated-users.md) | GET | Retrieves associated user accounts from Stackoverflow. |
| [List Elected Moderators](actions/list-elected-moderators.md) | GET | Retrieves elected moderators from Stackoverflow. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Stackoverflow. |
| [List Moderators](actions/moderators.md) | GET | Retrieves moderators from Stackoverflow. |
| [List Collective Users](actions/users-by-collective.md) | GET | Retrieves users for collectives from Stackoverflow. |

### User Timeline

| Action | Method | Description |
| --- | --- | --- |
| [List User Timeline](actions/list-user-timeline.md) | GET | Retrieves timeline entries for specific users from Stackoverflow. |

