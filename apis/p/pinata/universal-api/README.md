# <img src="https://images.mindcloud.co/apps/icons/pinata_1774987988806.png" alt="Pinata logo" width="28" height="28"> Pinata: Universal API

Upload, manage, and serve IPFS files and gateways

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pinata/latest
- **Category:** Content & Files / Storage
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pinata.cloud
- **Vendor API docs:** https://docs.pinata.cloud/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Test Authentication](actions/test-authentication.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinata/latest/actions/test-authentication?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Auth

| Action | Method | Description |
| --- | --- | --- |
| [Test Authentication](actions/test-authentication.md) | GET | Retrieves the current authentication status from Pinata. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Delete File by ID](actions/delete-file-by-id.md) | DELETE | Deletes an existing file from Pinata by ID. |
| [Get File by ID](actions/get-file-by-id.md) | GET | Retrieves a file from Pinata by ID. |
| [List Files](actions/list-files.md) | GET | Retrieves files from Pinata for a selected network. |
| [Pin by CID](actions/pin-by-cid.md) | POST | Creates a new pin request in Pinata by CID. |
| [Pin JSON](actions/pin-json.md) | POST | Creates a new pinned JSON object in Pinata. |
| [Update File](actions/update-file.md) | PUT | Updates an existing file in Pinata. |

### Gateway

| Action | Method | Description |
| --- | --- | --- |
| [Create Gateway](actions/create-gateway.md) | POST | Creates a new gateway in Pinata. |
| [Delete Gateway](actions/delete-gateway.md) | DELETE | Deletes an existing gateway from Pinata. |
| [Get Gateway Details](actions/get-gateway-details.md) | GET | Retrieves gateway details from Pinata. |
| [List Gateways](actions/list-gateways.md) | GET | Retrieves gateways from Pinata for the current account. |

### Gateway Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Time Interval Gateway Analytics](actions/get-time-interval-gateway-analytics.md) | GET | Retrieves time-interval gateway analytics from Pinata. |
| [Get Top Gateway Analytics](actions/get-top-gateway-analytics.md) | GET | Retrieves top gateway analytics from Pinata. |

### Gateway Domain

| Action | Method | Description |
| --- | --- | --- |
| [Get Gateway Domain Availability](actions/get-gateway-domain-availability.md) | GET | Retrieves gateway domain availability from Pinata. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Add File To Group](actions/add-file-to-group.md) | PUT | Updates a Pinata group by adding a file. |
| [Create Group](actions/create-group.md) | POST | Creates a new group in Pinata. |
| [Delete Group](actions/delete-group.md) | DELETE | Deletes an existing group from Pinata. |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from Pinata by ID. |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from Pinata for a selected network. |
| [Remove File From Group](actions/remove-file-from-group.md) | DELETE | Deletes a file from a Pinata group. |
| [Update Group](actions/update-group.md) | PUT | Updates an existing group in Pinata. |

### Pin Request

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Pin Request](actions/cancel-pin-request.md) | DELETE | Deletes an existing pin request from Pinata. |
| [Search Pin Requests](actions/search-pin-requests.md) | GET | Finds matching pin requests in Pinata. |

### Signature

| Action | Method | Description |
| --- | --- | --- |
| [Add Signature to CID](actions/add-signature-to-cid.md) | POST | Creates a new CID signature in Pinata. |
| [Get Signature for a CID](actions/get-signature-for-a-cid.md) | GET | Retrieves a CID signature from Pinata. |
| [Remove Signature from CID](actions/remove-signature-from-cid.md) | DELETE | Deletes an existing CID signature from Pinata. |

### Swap

| Action | Method | Description |
| --- | --- | --- |
| [Add Swap](actions/add-swap.md) | PUT | Updates a CID swap mapping in Pinata. |
| [Get Swap History](actions/get-swap-history.md) | GET | Retrieves CID swap history from Pinata. |
| [Remove Swap](actions/remove-swap.md) | DELETE | Deletes an existing CID swap from Pinata. |

### Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Data Usage](actions/get-data-usage.md) | GET | Retrieves pinned data usage from Pinata. |

