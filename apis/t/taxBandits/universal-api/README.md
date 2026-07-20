# <img src="https://images.mindcloud.co/apps/icons/images-15_1774901710075.jpeg" alt="TaxBandits logo" width="28" height="28"> TaxBandits: Universal API

TaxBandits API for tax filing workflows, business management, form status, and related compliance operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/taxBandits/latest
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.taxbandits.com/
- **Vendor API docs:** https://developer.taxbandits.com/docs/apireference/gettingstarted/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Test Connection](actions/test-connection.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/test-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### 1099 Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Create 1099 Transactions](actions/create1099-transactions.md) | POST | Creates 1099 transactions in TaxBandits. |
| [Delete 1099 Transactions](actions/delete1099-transactions.md) | DELETE | Deletes 1099 transactions from TaxBandits. |
| [List 1099 Transactions](actions/list1099-transactions.md) | GET | Retrieves 1099 transactions from TaxBandits. |

### 1099 Transaction Report

| Action | Method | Description |
| --- | --- | --- |
| [Get 1099 Transactions Report](actions/get1099-transactions-report.md) | GET | Retrieves a 1099 transactions report from TaxBandits. |

### Business

| Action | Method | Description |
| --- | --- | --- |
| [Create Business](actions/create-business.md) | POST | Creates a new business in TaxBandits. |
| [Delete Business](actions/delete-business.md) | DELETE | Deletes an existing business from TaxBandits. |
| [Get Business](actions/get-business.md) | GET | Retrieves a business from TaxBandits. |
| [Update Business](actions/update-business.md) | PUT | Updates an existing business in TaxBandits. |

### Business Link

| Action | Method | Description |
| --- | --- | --- |
| [Request Business by URL](actions/request-business-by-url.md) | GET | Retrieves a business request URL from TaxBandits. |

### Form W-9

| Action | Method | Description |
| --- | --- | --- |
| [Delete W-9](actions/delete-w9.md) | DELETE | Deletes a W-9 from TaxBandits. |
| [Get W-9](actions/get-w9.md) | GET | Retrieves a W-9 from TaxBandits. |
| [List W-9s](actions/list-w9s.md) | GET | Retrieves W-9 records from TaxBandits. |

### Form W-9 Request

| Action | Method | Description |
| --- | --- | --- |
| [Request W-9 by Email](actions/request-w9-by-email.md) | POST | Creates a W-9 request by email in TaxBandits. |
| [Request W-9 by URL](actions/request-w9-by-url.md) | POST | Creates a W-9 request URL in TaxBandits. |

### Form W-9 Status

| Action | Method | Description |
| --- | --- | --- |
| [Get W-9 Status](actions/get-w9-status.md) | GET | Retrieves W-9 status from TaxBandits. |

### Record

| Action | Method | Description |
| --- | --- | --- |
| [List Record IDs](actions/list-record-ids.md) | GET | Retrieves record IDs from TaxBandits. |
| [List Record IDs by Submission ID](actions/list-record-ids-by-submission-id.md) | GET | Retrieves record IDs for a submission in TaxBandits. |

### Submission

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Submission](actions/cancel-submission.md) | DELETE | Cancels an existing submission in TaxBandits. |
| [Get Submission ID by Record ID](actions/get-submission-id-by-record-id.md) | GET | Retrieves a submission ID by record ID in TaxBandits. |
| [List Submission IDs](actions/list-submission-ids.md) | GET | Retrieves submission IDs from TaxBandits. |
| [List Submission IDs by Business](actions/list-submission-ids-by-business.md) | GET | Retrieves submission IDs for a business in TaxBandits. |

### Tin Matching Request

| Action | Method | Description |
| --- | --- | --- |
| [Cancel TIN Matching Request](actions/cancel-tin-matching-request.md) | PUT | Cancels a TIN matching request in TaxBandits. |
| [List TIN Matching Requests](actions/list-tin-matching-requests.md) | GET | Retrieves TIN matching requests from TaxBandits. |
| [Request TIN Matching](actions/request-tin-matching.md) | POST | Creates a TIN matching request in TaxBandits. |

### Tin Matching Status

| Action | Method | Description |
| --- | --- | --- |
| [Get TIN Matching Status](actions/get-tin-matching-status.md) | GET | Retrieves TIN matching request status from TaxBandits. |

### Utility Ping

| Action | Method | Description |
| --- | --- | --- |
| [Test Connection](actions/test-connection.md) | GET | Retrieves TaxBandits API connection status and version details. |

### Wh Certificate

| Action | Method | Description |
| --- | --- | --- |
| [Get WH Certificate](actions/get-wh-certificate.md) | GET | Retrieves a withholding certificate from TaxBandits. |

### Wh Certificate Request

| Action | Method | Description |
| --- | --- | --- |
| [Request WH Certificate by Email](actions/request-wh-certificate-by-email.md) | POST | Creates a withholding certificate request by email in TaxBandits. |
| [Request WH Certificate by URL](actions/request-wh-certificate-by-url.md) | POST | Creates a withholding certificate request URL in TaxBandits. |

### Wh Certificate Status

| Action | Method | Description |
| --- | --- | --- |
| [Get WH Certificate Status](actions/get-wh-certificate-status.md) | GET | Retrieves withholding certificate status from TaxBandits. |

