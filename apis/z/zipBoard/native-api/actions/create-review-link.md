# Create Review Link with zipBoard

Creates a new review link in zipBoard.

## Endpoint

- **Method:** `POST`
- **Path:** `/shareurl`
- **Base URL:** `https://app.zipboard.co/api/v1`
- **Official documentation:** [Create Review Link](https://help.zipboard.co/article/180-api-for-review-links)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileid` | body | `string` | yes | File ID for the review link. |
| `projectid` | body | `string` | yes | Project ID for the review link. |
| `secure` | body | `boolean` | yes | Require the reviewer to sign up before review. |
| `type` | body | `string` | yes | Type of link: view&comment, fresh, or viewonly. |
