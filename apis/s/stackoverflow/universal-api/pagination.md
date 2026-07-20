# Stackoverflow Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Stackoverflow expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/advanced-search-questions?connectionId=$CONNECTION_ID&limit=25&offset=0&site=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Stackoverflow actions that support pagination

- [Advanced Search Questions](actions/advanced-search-questions.md)
- [Deauthenticate Access Tokens](actions/deauthenticate-access-tokens.md)
- [Get Answers](actions/get-answers.md)
- [Get Badges](actions/get-badges.md)
- [Get Collectives](actions/get-collectives.md)
- [Get Comments](actions/get-comments.md)
- [Get Posts](actions/get-posts.md)
- [Get Questions](actions/get-questions.md)
- [Get Tag Info](actions/get-tag-info.md)
- [Get Users](actions/get-users.md)
- [List Answer Comments](actions/list-answer-comments.md)
- [List Answers](actions/list-answers.md)
- [List Associated Users](actions/list-associated-users.md)
- [List Badge Recipients](actions/list-badge-recipients.md)
- [List Badge Recipients By Badge](actions/list-badge-recipients-by-badge.md)
- [List Badges](actions/list-badges.md)
- [List Badges By Name](actions/list-badges-by-name.md)
- [List Badges By Tag](actions/list-badges-by-tag.md)
- [List Collective Answers](actions/list-collective-answers.md)
- [List Collectives](actions/list-collectives.md)
- [List Comments](actions/list-comments.md)
- [List Comments By User To User](actions/list-comments-by-user-to-user.md)
- [List Elected Moderators](actions/list-elected-moderators.md)
- [List Errors](actions/list-errors.md)
- [List Featured Questions](actions/list-featured-questions.md)
- [List Linked Questions](actions/list-linked-questions.md)
- [List Post Comments](actions/list-post-comments.md)
- [List Posts](actions/list-posts.md)
- [List Privileges](actions/list-privileges.md)
- [List Question Answers](actions/list-question-answers.md)
- [List Question Comments](actions/list-question-comments.md)
- [List Question Timeline](actions/list-question-timeline.md)
- [List Questions](actions/list-questions.md)
- [List Related Questions](actions/list-related-questions.md)
- [List Related Tags](actions/list-related-tags.md)
- [List Sites](actions/list-sites.md)
- [List Tag FAQs](actions/list-tag-faqs.md)
- [List Tag Synonyms](actions/list-tag-synonyms.md)
- [List Tags](actions/list-tags.md)
- [List Top Answerers For Tag](actions/list-top-answerers-for-tag.md)
- [List Top Askers For Tag](actions/list-top-askers-for-tag.md)
- [List Unanswered Questions](actions/list-unanswered-questions.md)
- [List User Achievements](actions/list-user-achievements.md)
- [List User Answers](actions/list-user-answers.md)
- [List User Badges](actions/list-user-badges.md)
- [List User Comments](actions/list-user-comments.md)
- [List User Favorites](actions/list-user-favorites.md)
- [List User Questions](actions/list-user-questions.md)
- [List User Reputation](actions/list-user-reputation.md)
- [List User Reputation History](actions/list-user-reputation-history.md)
- [List User Timeline](actions/list-user-timeline.md)
- [List Users](actions/list-users.md)
- [Search Question Excerpts](actions/search-question-excerpts.md)
- [Search Questions](actions/search-questions.md)
