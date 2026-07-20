# Check Content for Spam with OOPSpam

Checks submitted content for spam in OOPSpam.

## Endpoint

- **Method:** `POST`
- **Path:** `/spamdetection`
- **Base URL:** `https://api.oopspam.com/v1`
- **Official documentation:** [Check Content for Spam](https://www.oopspam.com/docs/#spam-detection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | no | Message content to analyze for spam. |
| `senderIP` | body | `string` | no | IP address of the original sender. |
| `email` | body | `string` | no | Email address of the original sender. |
| `checkForLength` | body | `boolean` | no | Treat very short content as spam. |
| `blockTempEmail` | body | `boolean` | no | Block disposable email addresses. |
| `logIt` | body | `boolean` | no | Send this request to OOPSpam dashboard logs. |
| `source` | body | `string` | no | Unique source identifier required when logIt is true. |
| `context` | body | `string` | no | Business or website context used for contextual detection. |
| `blockVPN` | body | `boolean` | no | Block VPN, proxy, and Tor IPs. |
| `blockDC` | body | `boolean` | no | Block cloud provider and data center IPs. |
| `urlFriendly` | body | `boolean` | no | Reduce the impact of links on the spam score. |
| `allowedLanguages[]` | body | `array<string>` | no | Two-letter language codes that are allowed. |
| `allowedCountries[]` | body | `array<string>` | no | Two-letter country codes that are allowed. |
| `blockedCountries[]` | body | `array<string>` | no | Two-letter country codes that are blocked. |
