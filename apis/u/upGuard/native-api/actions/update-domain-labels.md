# Update Domain Labels with UpGuard

Updates labels for a domain in UpGuard.

## Endpoint

- **Method:** `PUT`
- **Path:** `/domain/labels`
- **Base URL:** `https://cyber-risk.upguard.com/api/public`
- **Official documentation:** [Update Domain Labels](https://cyber-risk.upguard.com/api/docs#operation/domain_update_labels)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hostname` | query | `string` | yes | The hostname to update labels for |
| `labels` | query | `string<string>` | yes | The labels to assign to the domain. You can pass an empty array to remove all labels. Send multiple values as a string separated by `,`. |
