# Create Share with Next Cloud OCS

Creates a new share in Next Cloud OCS.

## Endpoint

- **Method:** `POST`
- **Path:** `/ocs/v2.php/apps/files_sharing/api/v1/shares`
- **Base URL:** `https://demo2.nextcloud.com`
- **Official documentation:** [Create Share](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-share-api.html#create-a-new-share)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | body | `string` | yes | Path to the file or folder to share. |
| `shareType` | body | `number` | yes | Share type integer: 0 user, 1 group, 3 public link, 4 email, 6 federated, 7 circle, 10 Talk conversation. |
| `shareWith` | body | `string` | yes | Recipient user, group, email, federated cloud ID, circle ID, or conversation name. |
