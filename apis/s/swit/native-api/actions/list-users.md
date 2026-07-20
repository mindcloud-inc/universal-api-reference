# List Users with Swit

Retrieves users from Swit with paginated results.

## Endpoint

- **Method:** `GET`
- **Path:** `organization.user.list`
- **Base URL:** `https://openapi.swit.io`
- **Official documentation:** [List Users](https://tech-support.swit.io/books/swit-java-development-guide/page/9dfcd)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cnt` | query | `number` | yes | Number of users to return per page. |
| `page` | query | `number` | no | Page number to fetch. |
