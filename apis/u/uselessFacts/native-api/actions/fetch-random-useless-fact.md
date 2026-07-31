# Fetch Random Useless Fact with Useless Facts

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/facts/random`
- **Base URL:** `https://uselessfacts.jsph.pl`
- **Official documentation:** [Fetch Random Useless Fact](https://uselessfacts.jsph.pl/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language` | query | `list<string>` | no | Optional fact language. The provider documents English (en) and German (de). Accepted values: `de`, `en`. |
