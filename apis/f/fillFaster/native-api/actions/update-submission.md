# Update Submission with FillFaster

Updates an existing submission in FillFaster.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/submission/update`
- **Base URL:** `https://api.fillfaster.com`
- **Official documentation:** [Update Submission](https://documenter.getpostman.com/view/18912453/2s8ZDVZ3UJ#24a91702-5d18-436b-bdc0-4c5d77f2953d)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | Submission fields to update. |
| `sid` | body | `string` | yes | Submission identifier to update. |
