# Fetch Useless Fact of the Day with Useless Facts

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/facts/today`
- **Base URL:** `https://uselessfacts.jsph.pl`
- **Official documentation:** [Fetch Useless Fact of the Day](https://uselessfacts.jsph.pl/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language` | query | `list<string>` | no | Optional fact language. The provider documents English (en) and German (de). Accepted values: `de`, `en`. |
