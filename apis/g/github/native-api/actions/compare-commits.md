# Compare Two Commits with GitHub

## Endpoint

- **Method:** `GET`
- **Path:** `/repos/:owner/:repo/compare/:basehead`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [Compare Two Commits](https://docs.github.com/en/rest/commits/commits#compare-two-commits)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `basehead` | path | `string` | no | The base branch and head branch to compare, as BASE...HEAD (for example master...cirra/my-branch). |
| `owner` | path | `string` | no | The account owner of the repository. |
| `repo` | path | `string` | no | The name of the repository. |
