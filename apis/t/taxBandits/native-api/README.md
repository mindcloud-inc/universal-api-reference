# TaxBandits: Native API Reference

A consolidated summary of TaxBandits's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://developer.taxbandits.com/docs/apireference/gettingstarted/
- **API base URL:** `https://testapi.taxbandits.com/v1.7.3/`

## Authentication

### TaxBandits Access Token

Sandbox bearer token for TaxBandits API access. Generate it from your Client ID, Client Secret, and User Token outside the app until automatic token exchange is supported.

### Credentials

- **Access Token:** `accessToken` · required · Current TaxBandits bearer token. Expires hourly.

Send these headers with each API request:

```http
Authorization: Bearer <accessToken>
```

[Official authentication documentation](https://developer.taxbandits.com/docs/OAuth2.0Authentication)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Submission](actions/cancel-submission.md) | `POST Utility/CancelSubmission` | [docs](https://developer.taxbandits.com/docs/utility/cancelsubmission/) |
| [Cancel TIN Matching Request](actions/cancel-tin-matching-request.md) | `PUT TINMatchingRecipients/CancelRequest` | [docs](https://developer.taxbandits.com/docs/tinmatchingrecipients/cancel/) |
| [Create Business](actions/create-business.md) | `POST Business/Create` | [docs](https://developer.taxbandits.com/docs/business/create/) |
| [Create 1099 Transactions](actions/create1099-transactions.md) | `POST Form1099Transactions` | [docs](https://developer.taxbandits.com/docs/form1099transactions/post/) |
| [Delete Business](actions/delete-business.md) | `DELETE Business/Delete` | [docs](https://developer.taxbandits.com/docs/business/delete/) |
| [Delete W-9](actions/delete-w9.md) | `DELETE FormW9/Delete` | [docs](https://developer.taxbandits.com/docs/formw9/delete/) |
| [Delete 1099 Transactions](actions/delete1099-transactions.md) | `DELETE Form1099Transactions` | [docs](https://developer.taxbandits.com/docs/form1099transactions/delete/) |
| [Get Business](actions/get-business.md) | `GET Business/Get` | [docs](https://developer.taxbandits.com/docs/business/get/) |
| [Get Submission ID by Record ID](actions/get-submission-id-by-record-id.md) | `GET Utility/GetSubmissionIdByRecordId` | [docs](https://developer.taxbandits.com/docs/utility/getsubmissionidbyrecordid/) |
| [Get TIN Matching Status](actions/get-tin-matching-status.md) | `GET TINMatchingRecipients/Status` | [docs](https://developer.taxbandits.com/docs/tinmatchingrecipients/status/) |
| [Get W-9](actions/get-w9.md) | `GET FormW9/Get` | [docs](https://developer.taxbandits.com/docs/formw9/get/) |
| [Get W-9 Status](actions/get-w9-status.md) | `GET FormW9/Status` | [docs](https://developer.taxbandits.com/docs/formw9/status/) |
| [Get WH Certificate](actions/get-wh-certificate.md) | `GET WhCertificate/Get` | [docs](https://developer.taxbandits.com/docs/whcertificate/get/) |
| [Get WH Certificate Status](actions/get-wh-certificate-status.md) | `GET WhCertificate/Status` | [docs](https://developer.taxbandits.com/docs/whcertificate/status/) |
| [Get 1099 Transactions Report](actions/get1099-transactions-report.md) | `GET Reports/Form1099Transactions` | [docs](https://developer.taxbandits.com/docs/form1099transactions/report/) |
| [List Record IDs](actions/list-record-ids.md) | `GET Utility/GetRecordIds` | [docs](https://developer.taxbandits.com/docs/utility/getrecordids/) |
| [List Record IDs by Submission ID](actions/list-record-ids-by-submission-id.md) | `GET Utility/GetRecordIdBySubmissionId` | [docs](https://developer.taxbandits.com/docs/utility/getrecordidbysubmissionid/) |
| [List Submission IDs](actions/list-submission-ids.md) | `GET Utility/GetAllSubmissionId` | [docs](https://developer.taxbandits.com/docs/utility/getallsubmissionid/) |
| [List Submission IDs by Business](actions/list-submission-ids-by-business.md) | `GET Utility/GetSubmissionIdByBusiness` | [docs](https://developer.taxbandits.com/docs/utility/getsubmissionidbybusiness/) |
| [List TIN Matching Requests](actions/list-tin-matching-requests.md) | `GET TINMatchingRecipients/List` | [docs](https://developer.taxbandits.com/docs/tinmatchingrecipients/list/) |
| [List W-9s](actions/list-w9s.md) | `GET FormW9/List` | [docs](https://developer.taxbandits.com/docs/formw9/list/) |
| [List 1099 Transactions](actions/list1099-transactions.md) | `GET Form1099Transactions` | [docs](https://developer.taxbandits.com/docs/form1099transactions/get/) |
| [Request Business by URL](actions/request-business-by-url.md) | `GET Business/RequestByURL` | [docs](https://developer.taxbandits.com/docs/business/requestbyurl/) |
| [Request TIN Matching](actions/request-tin-matching.md) | `POST TINMatchingRecipients/Request` | [docs](https://developer.taxbandits.com/docs/tinmatchingrecipients/request/) |
| [Request W-9 by Email](actions/request-w9-by-email.md) | `POST FormW9/RequestByEmail` | [docs](https://developer.taxbandits.com/docs/formw9/requestbyemail/) |
| [Request W-9 by URL](actions/request-w9-by-url.md) | `POST FormW9/RequestByUrl` | [docs](https://developer.taxbandits.com/docs/formw9/requestbyurl/) |
| [Request WH Certificate by Email](actions/request-wh-certificate-by-email.md) | `POST WhCertificate/RequestByEmail` | [docs](https://developer.taxbandits.com/docs/whcertificate/requestbyemail/) |
| [Request WH Certificate by URL](actions/request-wh-certificate-by-url.md) | `POST WhCertificate/RequestByUrl` | [docs](https://developer.taxbandits.com/docs/whcertificate/requestbyurl/) |
| [Test Connection](actions/test-connection.md) | `GET Utility/Ping` | [docs](https://developer.taxbandits.com/docs/utility/ping/) |
| [Update Business](actions/update-business.md) | `PUT Business/Update` | [docs](https://developer.taxbandits.com/docs/business/update/) |
