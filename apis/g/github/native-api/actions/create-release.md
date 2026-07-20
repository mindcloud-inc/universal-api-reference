# Create Release with GitHub

Creates a release in a GitHub repository.

## Endpoint

- **Method:** `POST`
- **Path:** `/repos/:owner/:repo/releases`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [Create Release](https://docs.github.com/en/rest/releases/releases#create-a-release)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | Repository owner or organization login. |
| `repo` | path | `string` | yes | Repository name. |
| `tag_name` | body | `string` | yes | The name of the tag. |
| `target_commitish` | body | `string` | no | The branch or commit SHA where the tag should be created if the tag does not already exist. |
| `name` | body | `string` | no | The name of the release. |
| `body` | body | `string` | no | Text describing the contents of the tag. |
| `draft` | body | `boolean` | no | Whether to create the release as a draft. |
| `prerelease` | body | `boolean` | no | Whether to identify the release as a prerelease. |
| `discussion_category_name` | body | `string` | no | An existing discussion category to create and link to the release. |
| `generate_release_notes` | body | `boolean` | no | Whether to automatically generate the release name and body. |
| `make_latest` | body | `list<string>` | no | Whether this release should be set as the latest release for the repository. Accepted values: `0`, `1`, `2`. |
