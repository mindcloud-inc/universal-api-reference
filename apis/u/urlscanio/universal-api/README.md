# <img src="https://images.mindcloud.co/apps/icons/urlscan-icon_1775854573946.png" alt="urlscan.io logo" width="28" height="28"> urlscan.io: Universal API

urlscan.io provides APIs for submitting website scans, retrieving scan results, searching historical scans, and managing saved searches, subscriptions, channels, incidents, and other security observables.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/urlscanio/latest
- **Category:** IT Operations / Security & Compliance
- **Actions:** 50
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://urlscan.io
- **Vendor API docs:** https://docs.urlscan.io/guides/quickstart

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Quotas](actions/get-quotas.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/urlscanio/latest/actions/get-quotas?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (50)

### Brand

| Action | Method | Description |
| --- | --- | --- |
| [List Available Brands](actions/list-available-brands.md) | GET |  |

### Brand Summary

| Action | Method | Description |
| --- | --- | --- |
| [List Brand Summary](actions/list-brand-summary.md) | GET |  |

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [Create Channel](actions/create-channel.md) | POST |  |
| [Get Channel](actions/get-channel.md) | GET |  |
| [List Channels](actions/list-channels.md) | GET |  |
| [Update Channel](actions/update-channel.md) | PUT |  |

### Country

| Action | Method | Description |
| --- | --- | --- |
| [List Available Countries](actions/list-available-countries.md) | GET | Retrieves available scan countries from urlscan.io. |

### Data Dump File

| Action | Method | Description |
| --- | --- | --- |
| [List Data Dump Files](actions/list-data-dump-files.md) | GET |  |

### Data Dump Link

| Action | Method | Description |
| --- | --- | --- |
| [Get Data Dump Link](actions/get-data-dump-link.md) | GET |  |

### Dom Snapshot

| Action | Method | Description |
| --- | --- | --- |
| [Get DOM Snapshot](actions/get-dom-snapshot.md) | GET | Retrieves a scan DOM snapshot from urlscan.io. |

### File Download

| Action | Method | Description |
| --- | --- | --- |
| [Download File](actions/download-file.md) | GET | Retrieves a file from urlscan.io by file hash. |

### Hostname History

| Action | Method | Description |
| --- | --- | --- |
| [Get Hostname History](actions/get-hostname-history.md) | GET |  |

### Incident

| Action | Method | Description |
| --- | --- | --- |
| [Close Incident](actions/close-incident.md) | PUT | Updates an incident by closing it in urlscan.io. |
| [Copy Incident](actions/copy-incident.md) | POST | Creates a copy of an incident in urlscan.io. |
| [Create Incident](actions/create-incident.md) | POST | Creates a new incident in urlscan.io. |
| [Fork Incident](actions/fork-incident.md) | POST | Creates a fork of an incident in urlscan.io. |
| [Get Incident](actions/get-incident.md) | GET | Retrieves an existing incident from urlscan.io. |
| [Restart Incident](actions/restart-incident.md) | PUT | Updates an incident by restarting it in urlscan.io. |
| [Update Incident](actions/update-incident.md) | PUT | Updates an existing incident in urlscan.io. |

### Incident State

| Action | Method | Description |
| --- | --- | --- |
| [Get Incident States](actions/get-incident-states.md) | GET | Retrieves states for an incident in urlscan.io. |

### Live Scan

| Action | Method | Description |
| --- | --- | --- |
| [Discard Live Scan](actions/discard-live-scan.md) | DELETE |  |
| [Run Live Scan](actions/run-live-scan.md) | POST |  |
| [Store Live Scan](actions/store-live-scan.md) | PUT |  |

### Live Scan Resource

| Action | Method | Description |
| --- | --- | --- |
| [Get Live Scan Resource](actions/get-live-scan-resource.md) | GET |  |

### Live Scan Task

| Action | Method | Description |
| --- | --- | --- |
| [Submit Live Scan Task](actions/submit-live-scan-task.md) | POST |  |

### Live Scanner

| Action | Method | Description |
| --- | --- | --- |
| [List Live Scanners](actions/list-live-scanners.md) | GET |  |

### Malicious Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Get Malicious Lookup](actions/get-malicious-lookup.md) | GET |  |

### Phishing Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Phishfeed Results](actions/get-phishfeed-results.md) | GET |  |

### Quota

| Action | Method | Description |
| --- | --- | --- |
| [Get Quotas](actions/get-quotas.md) | GET | Retrieves your current API quotas from urlscan.io. |

### Response

| Action | Method | Description |
| --- | --- | --- |
| [Get Response Content](actions/get-response-content.md) | GET |  |

### Saved Search

| Action | Method | Description |
| --- | --- | --- |
| [Create Saved Search](actions/create-saved-search.md) | POST |  |
| [Delete Saved Search](actions/delete-saved-search.md) | DELETE |  |
| [List Saved Searches](actions/list-saved-searches.md) | GET |  |
| [Update Saved Search](actions/update-saved-search.md) | PUT |  |

### Saved Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Saved Search Results](actions/get-saved-search-results.md) | GET |  |

### Scan

| Action | Method | Description |
| --- | --- | --- |
| [Submit Scan](actions/submit-scan.md) | POST | Creates a new scan in urlscan.io. |

### Scan Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Scan Result](actions/get-scan-result.md) | GET | Retrieves a scan result from urlscan.io. |

### Scan Visibility

| Action | Method | Description |
| --- | --- | --- |
| [Reset Result Visibility](actions/reset-result-visibility.md) | DELETE | Deletes a scan result visibility override in urlscan.io. |
| [Update Result Visibility](actions/update-result-visibility.md) | PUT | Updates a scan result's visibility in urlscan.io. |

### Screenshot

| Action | Method | Description |
| --- | --- | --- |
| [Get Screenshot](actions/get-screenshot.md) | GET | Retrieves a scan screenshot from urlscan.io. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Historical Results](actions/search-historical-results.md) | GET | Retrieves historical scan results from urlscan.io. |

### Similar Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Similar Results](actions/get-similar-results.md) | GET |  |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscription](actions/create-subscription.md) | POST |  |
| [Delete Subscription](actions/delete-subscription.md) | DELETE |  |
| [List Subscriptions](actions/list-subscriptions.md) | GET |  |
| [Update Subscription](actions/update-subscription.md) | PUT |  |

### Subscription Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Subscription Results](actions/get-subscription-results.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |

### User Agent

| Action | Method | Description |
| --- | --- | --- |
| [List User Agents](actions/list-user-agents.md) | GET |  |

### Watchable Attribute

| Action | Method | Description |
| --- | --- | --- |
| [List Watchable Attributes](actions/list-watchable-attributes.md) | GET | Retrieves watchable incident attributes from urlscan.io. |

