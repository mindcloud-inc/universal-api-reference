# Verify Document Support with Recommand

Verifies document support for a Recommand recipient.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/verify-document-support`
- **Base URL:** `https://app.recommand.eu`
- **Official documentation:** [Verify Document Support](https://recommand.eu/en/reference/recipients/verify-document-support)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentType` | body | `string` | yes | The document type to verify. You can use a full document type ID, or the simplified versions (e.g. "invoice", "creditNote", "selfBillingInvoice", "selfBillingCreditNote", ...). |
| `peppolAddress` | body | `string` | yes | The Peppol address of the recipient to verify. |
