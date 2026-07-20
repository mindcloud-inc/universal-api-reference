# Search using SuiteQL with NetSuite - Basic

Finds NetSuite records using a SuiteQL query.

## Endpoint

- **Method:** `POST`
- **Path:** `/query/v1/suiteql`
- **Base URL:** `https://{accountDomain}.suitetalk.api.netsuite.com/services/rest`
- **Official documentation:** [Search using SuiteQL](https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/section_157909186990.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | body | `string` | no | SuiteQL query text to send as the q body parameter. |
