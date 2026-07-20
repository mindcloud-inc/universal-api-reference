# Frameshift: Get Sample QC Stats

Retrieves sample QC statistics from Frameshift.

```
GET https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/get-sample-qc-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frameshift `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/get-sample-qc-stats?connectionId=$CONNECTION_ID&project_id=1&filter=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project_id": "1",
  "filter": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/get-sample-qc-stats?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project_id` | number | yes |  |
| `filter` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bothMatesMapped": {
        "mean": {},
        "quartiles": [
          {}
        ],
        "standardDeviation": {},
        "whiskers": [
          {}
        ]
      },
      "chromCoverage": {
        "mean": {},
        "quartiles": [
          {}
        ],
        "standardDeviation": {},
        "whiskers": [
          {}
        ]
      },
      "coverageHist": {
        "mean": {},
        "quartiles": [
          {}
        ],
        "standardDeviation": {},
        "whiskers": [
          {}
        ]
      },
      "coverageHistIqr": {
        "mean": {},
        "quartiles": [
          {}
        ],
        "standardDeviation": {},
        "whiskers": [
          {}
        ]
      },
      "coverageHistNoOutliers": {
        "mean": {},
        "quartiles": [
          {}
        ],
        "standardDeviation": {},
        "whiskers": [
          {}
        ]
      },
      "duplicates": {
        "mean": {},
        "quartiles": [
          {}
        ],
        "standardDeviation": {},
        "whiskers": [
          {}
        ]
      },
      "failedQc": {
        "mean": {},
        "quartiles": [
          {}
        ],
        "standardDeviation": {},
        "whiskers": [
          {}
        ]
      },
      "firstMates": {
        "mean": {},
        "quartiles": [
          {}
        ],
        "standardDeviation": {},
        "whiskers": [
          {}
        ]
      },
      "forwardStrands": {
        "mean": {},
        "quartiles": [
          {}
        ],
        "standardDeviation": {},
        "whiskers": [
          {}
        ]
      },
      "fragHist": {
        "mean": {},
        "quartiles": [
          {}
        ],
        "standardDeviation": {},
        "whiskers": [
          {}
        ]
      },
      "lengthHist": {
        "mean": {},
        "quartiles": [
          {}
        ],
        "standardDeviation": {},
        "whiskers": [
          {}
        ]
      },
      "mappedReads": {
        "mean": {},
        "quartiles": [
          {}
        ],
        "standardDeviation": {},
        "whiskers": [
          {}
        ]
      },
      "mapqHist": {
        "mean": {},
        "quartiles": [
          {}
        ],
        "standardDeviation": {},
        "whiskers": [
          {}
        ]
      },
      "medianReadCoverage": {
        "mean": {},
        "quartiles": [
          {}
        ],
        "standardDeviation": {},
        "whiskers": [
          {}
        ]
      },
      "pairedEndReads": {
        "mean": {},
        "quartiles": [
          {}
        ],
        "standardDeviation": {},
        "whiskers": [
          {}
        ]
      },
      "properPairs": {
        "mean": {},
        "quartiles": [
          {}
        ],
        "standardDeviation": {},
        "whiskers": [
          {}
        ]
      },
      "reverseStrands": {
        "mean": {},
        "quartiles": [
          {}
        ],
        "standardDeviation": {},
        "whiskers": [
          {}
        ]
      },
      "secondMates": {
        "mean": {},
        "quartiles": [
          {}
        ],
        "standardDeviation": {},
        "whiskers": [
          {}
        ]
      },
      "singletons": {
        "mean": {},
        "quartiles": [
          {}
        ],
        "standardDeviation": {},
        "whiskers": [
          {}
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bothMatesMapped.mean` | object |  |
| `bothMatesMapped.quartiles[]` | object |  |
| `bothMatesMapped.standardDeviation` | object |  |
| `bothMatesMapped.whiskers[]` | object |  |
| `chromCoverage.mean` | object |  |
| `chromCoverage.quartiles[]` | object |  |
| `chromCoverage.standardDeviation` | object |  |
| `chromCoverage.whiskers[]` | object |  |
| `coverageHist.mean` | object |  |
| `coverageHist.quartiles[]` | object |  |
| `coverageHist.standardDeviation` | object |  |
| `coverageHist.whiskers[]` | object |  |
| `coverageHistIqr.mean` | object |  |
| `coverageHistIqr.quartiles[]` | object |  |
| `coverageHistIqr.standardDeviation` | object |  |
| `coverageHistIqr.whiskers[]` | object |  |
| `coverageHistNoOutliers.mean` | object |  |
| `coverageHistNoOutliers.quartiles[]` | object |  |
| `coverageHistNoOutliers.standardDeviation` | object |  |
| `coverageHistNoOutliers.whiskers[]` | object |  |
| `duplicates.mean` | object |  |
| `duplicates.quartiles[]` | object |  |
| `duplicates.standardDeviation` | object |  |
| `duplicates.whiskers[]` | object |  |
| `failedQc.mean` | object |  |
| `failedQc.quartiles[]` | object |  |
| `failedQc.standardDeviation` | object |  |
| `failedQc.whiskers[]` | object |  |
| `firstMates.mean` | object |  |
| `firstMates.quartiles[]` | object |  |
| `firstMates.standardDeviation` | object |  |
| `firstMates.whiskers[]` | object |  |
| `forwardStrands.mean` | object |  |
| `forwardStrands.quartiles[]` | object |  |
| `forwardStrands.standardDeviation` | object |  |
| `forwardStrands.whiskers[]` | object |  |
| `fragHist.mean` | object |  |
| `fragHist.quartiles[]` | object |  |
| `fragHist.standardDeviation` | object |  |
| `fragHist.whiskers[]` | object |  |
| `lengthHist.mean` | object |  |
| `lengthHist.quartiles[]` | object |  |
| `lengthHist.standardDeviation` | object |  |
| `lengthHist.whiskers[]` | object |  |
| `mappedReads.mean` | object |  |
| `mappedReads.quartiles[]` | object |  |
| `mappedReads.standardDeviation` | object |  |
| `mappedReads.whiskers[]` | object |  |
| `mapqHist.mean` | object |  |
| `mapqHist.quartiles[]` | object |  |
| `mapqHist.standardDeviation` | object |  |
| `mapqHist.whiskers[]` | object |  |
| `medianReadCoverage.mean` | object |  |
| `medianReadCoverage.quartiles[]` | object |  |
| `medianReadCoverage.standardDeviation` | object |  |
| `medianReadCoverage.whiskers[]` | object |  |
| `pairedEndReads.mean` | object |  |
| `pairedEndReads.quartiles[]` | object |  |
| `pairedEndReads.standardDeviation` | object |  |
| `pairedEndReads.whiskers[]` | object |  |
| `properPairs.mean` | object |  |
| `properPairs.quartiles[]` | object |  |
| `properPairs.standardDeviation` | object |  |
| `properPairs.whiskers[]` | object |  |
| `reverseStrands.mean` | object |  |
| `reverseStrands.quartiles[]` | object |  |
| `reverseStrands.standardDeviation` | object |  |
| `reverseStrands.whiskers[]` | object |  |
| `secondMates.mean` | object |  |
| `secondMates.quartiles[]` | object |  |
| `secondMates.standardDeviation` | object |  |
| `secondMates.whiskers[]` | object |  |
| `singletons.mean` | object |  |
| `singletons.quartiles[]` | object |  |
| `singletons.standardDeviation` | object |  |
| `singletons.whiskers[]` | object |  |

## Native endpoint

Through the native Frameshift API, this operation is `GET /v1/projects/:project_id/sample-qc-stats` (base URL `https://mosaic.frameshift.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sample-qc-stats.md) for the provider-specific parameters and requirements.

