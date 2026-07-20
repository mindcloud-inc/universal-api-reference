# <img src="https://images.mindcloud.co/apps/icons/prembly_1775064954602.png" alt="Prembly logo" width="28" height="28"> Prembly: Universal API

Identity verification, fraud prevention, and background-check APIs for emerging markets.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/prembly/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://prembly.com
- **Vendor API docs:** https://docs.prembly.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Wallet Balance](actions/get-wallet-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prembly/latest/actions/get-wallet-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Addressverification

| Action | Method | Description |
| --- | --- | --- |
| [Address Verification](actions/address-verification.md) | POST | Creates an address verification in Prembly. |

### Amlscreening

| Action | Method | Description |
| --- | --- | --- |
| [PEP and Sanction](actions/pep-and-sanction.md) | POST | Runs PEP and sanction screening in Prembly. |

### Bankaccount

| Action | Method | Description |
| --- | --- | --- |
| [Bank Account (Basic)](actions/bank-account-basic.md) | POST | Creates a basic bank account verification in Prembly. |

### Bankaccountcomparison

| Action | Method | Description |
| --- | --- | --- |
| [Account with Name Comparism](actions/account-with-name-comparism.md) | POST | Creates account name comparism verification in Prembly. |

### Bulkscan

| Action | Method | Description |
| --- | --- | --- |
| [Get Bulk Fraud Scan Details](actions/get-bulk-fraud-scan-details.md) | GET | Retrieves a bulk fraud scan from Prembly. |
| [List Bulk Scan](actions/list-bulk-scan.md) | GET | Retrieves bulk fraud scans from Prembly. |

### Candidaterequest

| Action | Method | Description |
| --- | --- | --- |
| [Create Candidate Request](actions/create-candidate-request.md) | POST | Creates a candidate request in Prembly. |
| [Get Candidate Request Detail](actions/get-candidate-request-detail.md) | GET | Retrieves a candidate request from Prembly. |
| [List Candidate Requests](actions/list-candidate-requests.md) | GET | Retrieves candidate requests from Prembly. |
| [Reinitiate Candidate Request](actions/reinitiate-candidate-request.md) | PUT | Reinitiates a candidate request in Prembly. |

### Checktype

| Action | Method | Description |
| --- | --- | --- |
| [List All Check Types](actions/list-all-check-types.md) | GET | Retrieves all check types from Prembly. |

### Companysearch

| Action | Method | Description |
| --- | --- | --- |
| [Company Search By Person](actions/company-search-by-person.md) | POST | Creates a company search by person in Prembly. |

### Companyverification

| Action | Method | Description |
| --- | --- | --- |
| [Company Search With Registration Number](actions/company-search-with-registration-number.md) | POST | Creates a company search by registration number in Prembly. |

### Country

| Action | Method | Description |
| --- | --- | --- |
| [List Countries](actions/list-countries.md) | GET | Retrieves countries from Prembly. |

### Countrychecktype

| Action | Method | Description |
| --- | --- | --- |
| [List Check Types by Country](actions/list-check-types-by-country.md) | GET | Retrieves check types by country from Prembly. |

### Custompackage

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Package](actions/create-custom-package.md) | POST | Creates a custom package in Prembly. |
| [Delete Custom Package](actions/delete-custom-package.md) | DELETE | Deletes a custom package from Prembly. |
| [Get Custom Package Detail](actions/get-custom-package-detail.md) | GET | Retrieves a custom package from Prembly. |
| [List Custom Packages](actions/list-custom-packages.md) | GET | Retrieves custom packages from Prembly. |
| [Update Custom Package](actions/update-custom-package.md) | PUT | Updates a custom package in Prembly. |

### Documentverification

| Action | Method | Description |
| --- | --- | --- |
| [Document Verification](actions/document-verification.md) | POST | Creates a document verification in Prembly. |
| [Document Verification with Face](actions/document-verification-with-face.md) | POST | Creates document verification with face in Prembly. |

### Facecomparison

| Action | Method | Description |
| --- | --- | --- |
| [Face Comparison](actions/face-comparison.md) | POST | Creates a face comparison in Prembly. |

### Facelivelinesscheck

| Action | Method | Description |
| --- | --- | --- |
| [Face Liveliness Check](actions/face-liveliness-check.md) | POST | Creates a face liveliness check in Prembly. |

### Facescan

| Action | Method | Description |
| --- | --- | --- |
| [Face Scan](actions/face-scan.md) | POST | Creates a face scan in Prembly. |

### Fraudreport

| Action | Method | Description |
| --- | --- | --- |
| [Get Fraud Report Detail](actions/get-fraud-report-detail.md) | GET | Retrieves a fraud report from Prembly. |
| [List Fraud Reports](actions/list-fraud-reports.md) | GET | Retrieves fraud reports from Prembly. |
| [Submit Fraud Report](actions/submit-fraud-report.md) | POST | Submits a fraud report to Prembly. |

### Geolocationverification

| Action | Method | Description |
| --- | --- | --- |
| [Geo-location](actions/geo-location.md) | POST | Creates a geolocation verification in Prembly. |

### Idscan

| Action | Method | Description |
| --- | --- | --- |
| [ID Scan](actions/id-scan.md) | POST | Creates an ID scan in Prembly. |

### Phoneverification

| Action | Method | Description |
| --- | --- | --- |
| [Advance Phone Number](actions/advance-phone-number.md) | POST | Creates an advanced phone number verification in Prembly. |
| [Basic Phone Number](actions/basic-phone-number.md) | POST | Creates a basic phone number verification in Prembly. |

### Sdksession

| Action | Method | Description |
| --- | --- | --- |
| [Get SDK Session](actions/get-sdk-session.md) | GET | Retrieves SDK sessions from Prembly. |

### Systempackage

| Action | Method | Description |
| --- | --- | --- |
| [Get System Package Detail](actions/get-system-package-detail.md) | GET | Retrieves a system package from Prembly. |
| [List System Packages](actions/list-system-packages.md) | GET | Retrieves system packages from Prembly. |

### Taxidverification

| Action | Method | Description |
| --- | --- | --- |
| [Tax Identification Number Check](actions/tax-identification-number-check.md) | POST | Creates a tax identification number check in Prembly. |

### Transactionmonitoring

| Action | Method | Description |
| --- | --- | --- |
| [Transaction Monitoring Screen Transaction](actions/transaction-monitoring-screen-transaction.md) | POST | Screens a transaction with Prembly monitoring. |

### Vehicleverification

| Action | Method | Description |
| --- | --- | --- |
| [VIN/CAR CHASIS](actions/vincar-chasis.md) | POST | Creates a VIN or chassis verification in Prembly. |

### Verificationstatus

| Action | Method | Description |
| --- | --- | --- |
| [Get Verification Status](actions/get-verification-status.md) | GET | Retrieves a verification status from Prembly. |

### Wallet

| Action | Method | Description |
| --- | --- | --- |
| [Get Wallet Balance](actions/get-wallet-balance.md) | GET | Retrieves a wallet balance from Prembly. |

