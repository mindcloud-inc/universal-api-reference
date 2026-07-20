# <img src="https://images.mindcloud.co/apps/icons/direct-mail-manager_1775248215714.png" alt="Direct Mail Manager logo" width="28" height="28"> Direct Mail Manager: Universal API

Direct Mail Manager helps teams manage recipient data, mailing lists, segments, artwork, postcards, letters, and sender addresses for direct mail operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/directMailManager/latest
- **Category:** Marketing / Advertising
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://directmailmanager.com
- **Vendor API docs:** https://apidocs.directmailmanager.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Mailing Lists](actions/list-mailing-lists.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/list-mailing-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Addresses

| Action | Method | Description |
| --- | --- | --- |
| [Attach Address To Mailing List](actions/attach-address-to-mailing-list.md) | PUT |  |
| [Create Address](actions/create-address.md) | POST |  |
| [Create Company Address](actions/create-company-address.md) | POST |  |
| [Detach Address From Mailing List](actions/detach-address-from-mailing-list.md) | PUT |  |
| [Import Addresses](actions/import-addresses.md) | POST |  |
| [List Addresses](actions/list-addresses.md) | GET |  |
| [List Company Addresses](actions/list-company-addresses.md) | GET |  |
| [List Mailing List Addresses](actions/list-mailing-list-addresses.md) | GET |  |
| [List Segment Addresses](actions/list-segment-addresses.md) | GET |  |
| [Retrieve Address](actions/retrieve-address.md) | GET |  |
| [Suppress Address](actions/suppress-address.md) | PUT |  |
| [Unsuppress Address](actions/unsuppress-address.md) | PUT |  |
| [Update Address](actions/update-address.md) | PUT |  |

### Audiences

| Action | Method | Description |
| --- | --- | --- |
| [Create Mailing List](actions/create-mailing-list.md) | POST |  |
| [Delete Mailing List](actions/delete-mailing-list.md) | DELETE |  |
| [Get Mailing List](actions/get-mailing-list.md) | GET |  |
| [List Mailing Lists](actions/list-mailing-lists.md) | GET |  |
| [Update Mailing List](actions/update-mailing-list.md) | PUT |  |

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Create Letter](actions/create-letter.md) | POST |  |
| [Create Postcard](actions/create-postcard.md) | POST |  |
| [List Letters](actions/list-letters.md) | GET |  |
| [List Postcards](actions/list-postcards.md) | GET |  |

### Segments

| Action | Method | Description |
| --- | --- | --- |
| [Create Segment](actions/create-segment.md) | POST |  |
| [Get Segment](actions/get-segment.md) | GET |  |
| [List Segments](actions/list-segments.md) | GET |  |
| [Update Segment](actions/update-segment.md) | PUT |  |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Field](actions/create-custom-field.md) | POST |  |
| [Get Custom Field](actions/get-custom-field.md) | GET |  |
| [List Custom Fields](actions/list-custom-fields.md) | GET |  |
| [Update Custom Field](actions/update-custom-field.md) | PUT |  |

