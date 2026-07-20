# List Submission Posts with Tumblr

Retrieves submission posts from a Tumblr blog.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/blog/:blogIdentifier/posts/submission`
- **Base URL:** `https://api.tumblr.com`
- **Official documentation:** [List Submission Posts](https://www.tumblr.com/docs/en/api/v2#postssubmission--retrieve-submission-posts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blogIdentifier` | path | `string` | yes | Any Tumblr blog identifier for the target blog. |
| `filter` | query | `list<string>` | no | Format to return instead of default HTML output. Accepted values: `raw`, `text`. |
