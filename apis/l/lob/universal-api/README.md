# <img src="https://images.mindcloud.co/apps/icons/lob_1773846395659.png" alt="Lob logo" width="28" height="28"> Lob: Universal API

Send direct mail, verify addresses, and manage Lob mailpieces.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lob/latest
- **Actions:** 27
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.lob.com
- **Vendor API docs:** https://docs.lob.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Addresses](actions/list-addresses.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lob/latest/actions/list-addresses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (27)

### Address

| Action | Method | Description |
| --- | --- | --- |
| [Create Address](actions/create-address.md) | POST |  |
| [Delete Address](actions/delete-address.md) | DELETE |  |
| [List Addresses](actions/list-addresses.md) | GET |  |
| [Retrieve Address](actions/retrieve-address.md) | GET |  |

### Bank Accounts

| Action | Method | Description |
| --- | --- | --- |
| [Create Bank Account](actions/create-bank-account.md) | POST |  |
| [Delete Bank Account](actions/delete-bank-account.md) | DELETE |  |
| [List Bank Accounts](actions/list-bank-accounts.md) | GET |  |
| [Retrieve Bank Account](actions/retrieve-bank-account.md) | GET |  |
| [Verify Bank Account](actions/verify-bank-account.md) | PUT |  |

### Check

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Check](actions/cancel-check.md) | DELETE |  |
| [Create Check](actions/create-check.md) | POST |  |
| [List Checks](actions/list-checks.md) | GET |  |
| [Retrieve Check](actions/retrieve-check.md) | GET |  |

### International Verification

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Verify International Addresses](actions/bulk-verify-international-addresses.md) | POST |  |
| [Verify International Address](actions/verify-international-address.md) | POST |  |

### Letter

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Letter](actions/cancel-letter.md) | DELETE |  |
| [Create Letter](actions/create-letter.md) | POST |  |
| [List Letters](actions/list-letters.md) | GET |  |
| [Retrieve Letter](actions/retrieve-letter.md) | GET |  |

### Postcard

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Postcard](actions/cancel-postcard.md) | DELETE |  |
| [Create Postcard](actions/create-postcard.md) | POST |  |
| [List Postcards](actions/list-postcards.md) | GET |  |
| [Retrieve Postcard](actions/retrieve-postcard.md) | GET |  |

### Us Autocompletion

| Action | Method | Description |
| --- | --- | --- |
| [Autocomplete US Addresses](actions/autocomplete-us-addresses.md) | GET |  |

### Us Verification

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Verify US Addresses](actions/bulk-verify-us-addresses.md) | POST |  |
| [Verify US Address](actions/verify-us-address.md) | POST |  |

### Us Zip Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Lookup US ZIP Code](actions/lookup-uszip-code.md) | GET |  |

