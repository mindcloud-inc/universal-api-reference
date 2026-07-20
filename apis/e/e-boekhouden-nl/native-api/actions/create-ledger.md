# Create Ledger with e-Boekhouden.nl

Creates a new ledger in e-Boekhouden.nl.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/ledger`
- **Base URL:** `https://api.e-boekhouden.nl`
- **API:** rest
- **Official documentation:** [Create Ledger](https://api.e-boekhouden.nl/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | body | `string` | yes | The code of the ledger. Error codes LEDG_001 Code is missing. LEDG_002 Code is too long. |
| `description` | body | `string` | yes | The description of the ledger. Error codes LEDG_003 Description is missing. LEDG_004 Description is too long. |
| `category` | body | `string` | no | A list of ledger categories is displayed below. Only these values may be used in `POST` and `PATCH` operations: `["BAL", "VW", "FIN", "DEB", "CRED"]`. \| Value \| Description \| \|---\|---\| \| BAL \| Balance \| \| VW \| Profit and loss \| \| AF6 \| Turnover tax low rate \| \| AF19 \| Turnover tax high rate \| \| AFOVERIG \| Turnover tax other \| \| VOOR \| Input tax \| \| BTWRC \| VAT current account \| \| FIN \| Liquid Assets \| \| DEB \| Debtors \| \| CRED \| Creditors \| \| AF \| Turnover tax \| |
| `group` | body | `string` | no | The group of the ledger. Error codes LEDG_007 Group is missing. |
