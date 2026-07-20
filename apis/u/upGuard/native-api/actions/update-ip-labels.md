# Update IP Labels with UpGuard

Updates labels for an IP address in UpGuard.

## Endpoint

- **Method:** `PUT`
- **Path:** `/ip/labels`
- **Base URL:** `https://cyber-risk.upguard.com/api/public`
- **Official documentation:** [Update IP Labels](https://cyber-risk.upguard.com/api/docs#operation/ip_update_labels)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ip` | query | `string` | yes | The IP to update labels for |
| `labels` | query | `string<string>` | yes | The labels to assign to the IP. You can pass an empty array to remove all labels. Send multiple values as a string separated by `,`. |
