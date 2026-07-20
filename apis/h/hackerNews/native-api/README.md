# Hacker News: Native API Reference

A consolidated summary of Hacker News's API configuration and 50 documented operations, with links to official documentation.

- **Official docs:** https://github.com/HackerNews/API
- **API base URL:** `https://hacker-news.firebaseio.com/v0`

## Authentication

### No Auth

Public Hacker News API access does not require authentication.

This API does not require request authentication.

[Official authentication documentation](https://github.com/HackerNews/API)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (50 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Ask Story](actions/get-ask-story.md) | `GET /item/:id.json` | [docs](https://github.com/HackerNews/API#items) |
| [Get Ask Story ID By Rank](actions/get-ask-story-id-by-rank.md) | `GET /askstories/:index.json` | [docs](https://github.com/HackerNews/API#ask-show-and-job-stories) |
| [Get Ask Story IDs](actions/get-ask-story-ids.md) | `GET /askstories.json` | [docs](https://github.com/HackerNews/API#ask-show-and-job-stories) |
| [Get Best Story ID By Rank](actions/get-best-story-id-by-rank.md) | `GET /beststories/:index.json` | [docs](https://github.com/HackerNews/API#new-top-and-best-stories) |
| [Get Best Story IDs](actions/get-best-story-ids.md) | `GET /beststories.json` | [docs](https://github.com/HackerNews/API#new-top-and-best-stories) |
| [Get Comment](actions/get-comment.md) | `GET /item/:id.json` | [docs](https://github.com/HackerNews/API#items) |
| [Get Item](actions/get-item.md) | `GET /item/:id.json` | [docs](https://github.com/HackerNews/API#items) |
| [Get Item Author](actions/get-item-author.md) | `GET /item/:id/by.json` | [docs](https://github.com/HackerNews/API#items) |
| [Get Item Child ID By Index](actions/get-item-child-id-by-index.md) | `GET /item/:id/kids/:index.json` | [docs](https://github.com/HackerNews/API#items) |
| [Get Item Child IDs](actions/get-item-child-ids.md) | `GET /item/:id/kids.json` | [docs](https://github.com/HackerNews/API#items) |
| [Get Item Dead Flag](actions/get-item-dead-flag.md) | `GET /item/:id/dead.json` | [docs](https://github.com/HackerNews/API#items) |
| [Get Item Deleted Flag](actions/get-item-deleted-flag.md) | `GET /item/:id/deleted.json` | [docs](https://github.com/HackerNews/API#items) |
| [Get Item Descendant Count](actions/get-item-descendant-count.md) | `GET /item/:id/descendants.json` | [docs](https://github.com/HackerNews/API#items) |
| [Get Item ID](actions/get-item-id.md) | `GET /item/:id/id.json` | [docs](https://github.com/HackerNews/API#items) |
| [Get Item Parent](actions/get-item-parent.md) | `GET /item/:id/parent.json` | [docs](https://github.com/HackerNews/API#items) |
| [Get Item Poll ID](actions/get-item-poll-id.md) | `GET /item/:id/poll.json` | [docs](https://github.com/HackerNews/API#items) |
| [Get Item Score](actions/get-item-score.md) | `GET /item/:id/score.json` | [docs](https://github.com/HackerNews/API#items) |
| [Get Item Text](actions/get-item-text.md) | `GET /item/:id/text.json` | [docs](https://github.com/HackerNews/API#items) |
| [Get Item Time](actions/get-item-time.md) | `GET /item/:id/time.json` | [docs](https://github.com/HackerNews/API#items) |
| [Get Item Title](actions/get-item-title.md) | `GET /item/:id/title.json` | [docs](https://github.com/HackerNews/API#items) |
| [Get Item Type](actions/get-item-type.md) | `GET /item/:id/type.json` | [docs](https://github.com/HackerNews/API#items) |
| [Get Item URL](actions/get-item-url.md) | `GET /item/:id/url.json` | [docs](https://github.com/HackerNews/API#items) |
| [Get Job](actions/get-job.md) | `GET /item/:id.json` | [docs](https://github.com/HackerNews/API#items) |
| [Get Job Story ID By Rank](actions/get-job-story-id-by-rank.md) | `GET /jobstories/:index.json` | [docs](https://github.com/HackerNews/API#ask-show-and-job-stories) |
| [Get Job Story IDs](actions/get-job-story-ids.md) | `GET /jobstories.json` | [docs](https://github.com/HackerNews/API#ask-show-and-job-stories) |
| [Get Max Item ID](actions/get-max-item-id.md) | `GET /maxitem.json` | [docs](https://github.com/HackerNews/API#max-item-id) |
| [Get New Story ID By Rank](actions/get-new-story-id-by-rank.md) | `GET /newstories/:index.json` | [docs](https://github.com/HackerNews/API#new-top-and-best-stories) |
| [Get New Story IDs](actions/get-new-story-ids.md) | `GET /newstories.json` | [docs](https://github.com/HackerNews/API#new-top-and-best-stories) |
| [Get Poll](actions/get-poll.md) | `GET /item/:id.json` | [docs](https://github.com/HackerNews/API#items) |
| [Get Poll Option](actions/get-poll-option.md) | `GET /item/:id.json` | [docs](https://github.com/HackerNews/API#items) |
| [Get Poll Option ID By Index](actions/get-poll-option-id-by-index.md) | `GET /item/:id/parts/:index.json` | [docs](https://github.com/HackerNews/API#items) |
| [Get Poll Option IDs](actions/get-poll-option-ids.md) | `GET /item/:id/parts.json` | [docs](https://github.com/HackerNews/API#items) |
| [Get Show Story](actions/get-show-story.md) | `GET /item/:id.json` | [docs](https://github.com/HackerNews/API#items) |
| [Get Show Story ID By Rank](actions/get-show-story-id-by-rank.md) | `GET /showstories/:index.json` | [docs](https://github.com/HackerNews/API#ask-show-and-job-stories) |
| [Get Show Story IDs](actions/get-show-story-ids.md) | `GET /showstories.json` | [docs](https://github.com/HackerNews/API#ask-show-and-job-stories) |
| [Get Story](actions/get-story.md) | `GET /item/:id.json` | [docs](https://github.com/HackerNews/API#items) |
| [Get Top Story ID By Rank](actions/get-top-story-id-by-rank.md) | `GET /topstories/:index.json` | [docs](https://github.com/HackerNews/API#new-top-and-best-stories) |
| [Get Top Story IDs](actions/get-top-story-ids.md) | `GET /topstories.json` | [docs](https://github.com/HackerNews/API#new-top-and-best-stories) |
| [Get Updated Item ID By Index](actions/get-updated-item-id-by-index.md) | `GET /updates/items/:index.json` | [docs](https://github.com/HackerNews/API#changed-items-and-profiles) |
| [Get Updated Item IDs](actions/get-updated-item-ids.md) | `GET /updates/items.json` | [docs](https://github.com/HackerNews/API#changed-items-and-profiles) |
| [Get Updated Profile ID By Index](actions/get-updated-profile-id-by-index.md) | `GET /updates/profiles/:index.json` | [docs](https://github.com/HackerNews/API#changed-items-and-profiles) |
| [Get Updated Profile IDs](actions/get-updated-profile-ids.md) | `GET /updates/profiles.json` | [docs](https://github.com/HackerNews/API#changed-items-and-profiles) |
| [Get Updates](actions/get-updates.md) | `GET /updates.json` | [docs](https://github.com/HackerNews/API#changed-items-and-profiles) |
| [Get User](actions/get-user.md) | `GET /user/:id.json` | [docs](https://github.com/HackerNews/API#users) |
| [Get User About](actions/get-user-about.md) | `GET /user/:id/about.json` | [docs](https://github.com/HackerNews/API#users) |
| [Get User Created](actions/get-user-created.md) | `GET /user/:id/created.json` | [docs](https://github.com/HackerNews/API#users) |
| [Get User ID](actions/get-user-id.md) | `GET /user/:id/id.json` | [docs](https://github.com/HackerNews/API#users) |
| [Get User Karma](actions/get-user-karma.md) | `GET /user/:id/karma.json` | [docs](https://github.com/HackerNews/API#users) |
| [Get User Submission ID By Index](actions/get-user-submission-id-by-index.md) | `GET /user/:id/submitted/:index.json` | [docs](https://github.com/HackerNews/API#users) |
| [Get User Submission IDs](actions/get-user-submission-ids.md) | `GET /user/:id/submitted.json` | [docs](https://github.com/HackerNews/API#users) |
