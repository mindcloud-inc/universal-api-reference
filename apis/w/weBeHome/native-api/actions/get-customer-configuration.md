# Get Customer Configuration with WeBeHome

## Endpoint

- **Method:** `GET`
- **Path:** `WebAPI.aspx`
- **Base URL:** `https://webehome.com/API`
- **Official documentation:** [Get Customer Configuration](https://www.webehome.com/Doc/WBH_Customer_API.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `HtmlTable` | query | `string` | yes | Return format. Defaults to plain delimited text when omitted. Accepted values: `0`, `1`. |
| `Heading` | query | `string` | yes | Include column headings. Defaults to Yes when omitted. Accepted values: `0`, `1`. |
