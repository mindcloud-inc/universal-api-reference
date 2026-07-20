# Update List Details with Zoho Campaigns

Updates a Zoho Campaigns mailing list.

## Endpoint

- **Method:** `POST`
- **Path:** `/updatelistdetails`
- **Base URL:** `https://campaigns.zoho.com/api/v1.1`
- **Official documentation:** [Update List Details](https://www.zoho.com/campaigns/help/developers/update-list.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listkey` | query | `list<string>` | yes | List key to update. |
| `newlistname` | query | `string` | yes | New name to apply to the mailing list. |
| `signupform` | query | `string` | yes | Whether the mailing list signup form stays public or private. Accepted values: `0`, `1`. |
