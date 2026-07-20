# List Post Tags with Postpone

Retrieves post tags from Postpone.

## Endpoint

- **Method:** `POST`
- **Path:** `/gql`
- **Base URL:** `https://api.postpone.app`
- **Official documentation:** [List Post Tags](https://developers.postpone.app/scheduling-posts/post-tags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.activeOnly` | body | `boolean` | no | When true, returns only active tags. Defaults to true. |
