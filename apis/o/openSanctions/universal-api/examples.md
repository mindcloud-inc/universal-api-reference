# OpenSanctions Universal API Examples

These examples use the MindCloud API key and OpenSanctions connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Entity



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openSanctions/latest/actions/get-entity?connectionId=$CONNECTION_ID&entity_id=Q7747" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entity_id": "Q7747"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openSanctions/latest/actions/get-entity?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "caption": "string",
      "datasets": [
        "string"
      ],
      "firstSeen": "string",
      "id": "string",
      "lastChange": "string",
      "lastSeen": "string",
      "properties": {
        "address": [
          "string"
        ],
        "addressEntity": [
          {
            "caption": "string",
            "datasets": [
              "string"
            ],
            "firstSeen": "string",
            "id": "string",
            "lastChange": "string",
            "lastSeen": "string",
            "properties": {
              "city": [
                "string"
              ],
              "country": [
                "string"
              ],
              "full": [
                "string"
              ],
              "street": [
                "string"
              ]
            },
            "schema": "string",
            "target": true
          }
        ],
        "alias": [
          "string"
        ],
        "associations": [
          {
            "caption": "string",
            "datasets": [
              "string"
            ],
            "firstSeen": "string",
            "id": "string",
            "lastChange": "string",
            "lastSeen": "string",
            "properties": {
              "associate": [
                "string"
              ],
              "person": [
                {
                  "caption": "string",
                  "datasets": [
                    "string"
                  ],
                  "firstSeen": "string",
                  "id": "string",
                  "lastChange": "string",
                  "lastSeen": "string",
                  "properties": {
                    "address": [
                      "string"
                    ],
                    "addressEntity": [
                      "string"
                    ],
                    "alias": [
                      "string"
                    ],
                    "birthCountry": [
                      "string"
                    ],
                    "birthDate": [
                      "string"
                    ],
                    "birthPlace": [
                      "string"
                    ],
                    "citizenship": [
                      "string"
                    ],
                    "country": [
                      "string"
                    ],
                    "createdAt": [
                      "string"
                    ],
                    "education": [
                      "string"
                    ],
                    "fatherName": [
                      "Ava Chen"
                    ],
                    "firstName": [
                      "Ava"
                    ],
                    "gender": [
                      "string"
                    ],
                    "innCode": [
                      "string"
                    ],
                    "lastName": [
                      "Chen"
                    ],
                    "middleName": [
                      "Ava Chen"
                    ],
                    "modifiedAt": [
                      "string"
                    ],
                    "name": [
                      "Ava Chen"
                    ],
                    "nationality": [
                      "string"
                    ],
                    "notes": [
                      "string"
                    ],
                    "position": [
                      "string"
                    ],
                    "programId": [
                      "string"
                    ],
                    "sourceUrl": [
                      "https://example.com"
                    ],
                    "topics": [
                      "string"
                    ],
                    "uniqueEntityId": [
                      "string"
                    ],
                    "wikidataId": [
                      "string"
                    ],
                    "wikipediaUrl": [
                      "https://example.com"
                    ]
                  },
                  "referents": [
                    "string"
                  ],
                  "schema": "string",
                  "target": true
                }
              ],
              "relationship": [
                "string"
              ],
              "sourceUrl": [
                "https://example.com"
              ]
            },
            "schema": "string",
            "target": true
          }
        ],
        "birthCountry": [
          "string"
        ],
        "birthDate": [
          "string"
        ],
        "birthPlace": [
          "string"
        ],
        "citizenship": [
          "string"
        ],
        "classification": [
          "string"
        ],
        "country": [
          "string"
        ],
        "createdAt": [
          "string"
        ],
        "description": [
          "string"
        ],
        "documentedBy": [
          {
            "caption": "string",
            "datasets": [
              "string"
            ],
            "firstSeen": "string",
            "id": "string",
            "lastChange": "string",
            "lastSeen": "string",
            "properties": {
              "date": [
                "string"
              ],
              "document": [
                {
                  "caption": "string",
                  "datasets": [
                    "string"
                  ],
                  "firstSeen": "string",
                  "id": "string",
                  "lastChange": "string",
                  "lastSeen": "string",
                  "properties": {
                    "publishedAt": [
                      "string"
                    ],
                    "sourceUrl": [
                      "https://example.com"
                    ],
                    "title": [
                      "string"
                    ]
                  },
                  "schema": "string",
                  "target": true
                }
              ],
              "entity": [
                "string"
              ]
            },
            "schema": "string",
            "target": true
          }
        ],
        "education": [
          "string"
        ],
        "ethnicity": [
          "string"
        ],
        "familyPerson": [
          {
            "caption": "string",
            "datasets": [
              "string"
            ],
            "firstSeen": "string",
            "id": "string",
            "lastChange": "string",
            "lastSeen": "string",
            "properties": {
              "person": [
                "string"
              ],
              "relationship": [
                "string"
              ],
              "relative": [
                {
                  "caption": "string",
                  "datasets": [
                    "string"
                  ],
                  "firstSeen": "string",
                  "id": "string",
                  "lastChange": "string",
                  "lastSeen": "string",
                  "properties": {
                    "alias": [
                      "string"
                    ],
                    "birthDate": [
                      "string"
                    ],
                    "birthPlace": [
                      "string"
                    ],
                    "citizenship": [
                      "string"
                    ],
                    "firstName": [
                      "Ava"
                    ],
                    "gender": [
                      "string"
                    ],
                    "lastName": [
                      "Chen"
                    ],
                    "name": [
                      "Ava Chen"
                    ],
                    "notes": [
                      "string"
                    ],
                    "topics": [
                      "string"
                    ],
                    "weakAlias": [
                      "string"
                    ],
                    "wikidataId": [
                      "string"
                    ],
                    "wikipediaUrl": [
                      "https://example.com"
                    ]
                  },
                  "schema": "string",
                  "target": true
                }
              ],
              "sourceUrl": [
                "https://example.com"
              ]
            },
            "referents": [
              "string"
            ],
            "schema": "string",
            "target": true
          }
        ],
        "familyRelative": [
          {
            "caption": "string",
            "datasets": [
              "string"
            ],
            "firstSeen": "string",
            "id": "string",
            "lastChange": "string",
            "lastSeen": "string",
            "properties": {
              "person": [
                {
                  "caption": "string",
                  "datasets": [
                    "string"
                  ],
                  "firstSeen": "string",
                  "id": "string",
                  "lastChange": "string",
                  "lastSeen": "string",
                  "properties": {
                    "address": [
                      "string"
                    ],
                    "alias": [
                      "string"
                    ],
                    "birthCountry": [
                      "string"
                    ],
                    "birthDate": [
                      "string"
                    ],
                    "birthPlace": [
                      "string"
                    ],
                    "citizenship": [
                      "string"
                    ],
                    "country": [
                      "string"
                    ],
                    "createdAt": [
                      "string"
                    ],
                    "education": [
                      "string"
                    ],
                    "fatherName": [
                      "Ava Chen"
                    ],
                    "firstName": [
                      "Ava"
                    ],
                    "gender": [
                      "string"
                    ],
                    "idNumber": [
                      "string"
                    ],
                    "innCode": [
                      "string"
                    ],
                    "lastName": [
                      "Chen"
                    ],
                    "middleName": [
                      "Ava Chen"
                    ],
                    "modifiedAt": [
                      "string"
                    ],
                    "name": [
                      "Ava Chen"
                    ],
                    "nationality": [
                      "string"
                    ],
                    "notes": [
                      "string"
                    ],
                    "position": [
                      "string"
                    ],
                    "programId": [
                      "string"
                    ],
                    "sourceUrl": [
                      "https://example.com"
                    ],
                    "taxNumber": [
                      "string"
                    ],
                    "topics": [
                      "string"
                    ],
                    "uniqueEntityId": [
                      "string"
                    ],
                    "wikidataId": [
                      "string"
                    ],
                    "wikipediaUrl": [
                      "https://example.com"
                    ]
                  },
                  "referents": [
                    "string"
                  ],
                  "schema": "string",
                  "target": true
                }
              ],
              "relationship": [
                "string"
              ],
              "relative": [
                "string"
              ]
            },
            "schema": "string",
            "target": true
          }
        ],
        "fatherName": [
          "Ava Chen"
        ],
        "firstName": [
          "Ava"
        ],
        "gender": [
          "string"
        ],
        "identification": [
          {
            "caption": "string",
            "datasets": [
              "string"
            ],
            "firstSeen": "string",
            "id": "string",
            "lastChange": "string",
            "lastSeen": "string",
            "properties": {
              "holder": [
                "string"
              ]
            },
            "schema": "string",
            "target": true
          }
        ],
        "lastName": [
          "Chen"
        ],
        "membershipMember": [
          {
            "caption": "string",
            "datasets": [
              "string"
            ],
            "firstSeen": "string",
            "id": "string",
            "lastChange": "string",
            "lastSeen": "string",
            "properties": {
              "member": [
                "string"
              ],
              "organization": [
                {
                  "caption": "string",
                  "datasets": [
                    "string"
                  ],
                  "firstSeen": "string",
                  "id": "string",
                  "lastChange": "string",
                  "lastSeen": "string",
                  "properties": {
                    "address": [
                      "string"
                    ],
                    "country": [
                      "string"
                    ],
                    "description": [
                      "string"
                    ],
                    "mainCountry": [
                      "string"
                    ],
                    "name": [
                      "Ava Chen"
                    ],
                    "permId": [
                      "string"
                    ],
                    "topics": [
                      "string"
                    ],
                    "website": [
                      "string"
                    ]
                  },
                  "referents": [
                    "string"
                  ],
                  "schema": "string",
                  "target": true
                }
              ],
              "role": [
                "string"
              ]
            },
            "schema": "string",
            "target": true
          }
        ],
        "middleName": [
          "Ava Chen"
        ],
        "modifiedAt": [
          "string"
        ],
        "name": [
          "Ava Chen"
        ],
        "nationality": [
          "string"
        ],
        "notes": [
          "string"
        ],
        "ownershipOwner": [
          {
            "caption": "string",
            "datasets": [
              "string"
            ],
            "firstSeen": "string",
            "id": "string",
            "lastChange": "string",
            "lastSeen": "string",
            "properties": {
              "asset": [
                {
                  "caption": "string",
                  "datasets": [
                    "string"
                  ],
                  "firstSeen": "string",
                  "id": "string",
                  "lastChange": "string",
                  "lastSeen": "string",
                  "properties": {
                    "buildDate": [
                      "string"
                    ],
                    "callSign": [
                      "string"
                    ],
                    "deadweightTonnage": [
                      "string"
                    ],
                    "description": [
                      "string"
                    ],
                    "flag": [
                      "string"
                    ],
                    "grossRegisteredTonnage": [
                      "string"
                    ],
                    "imoNumber": [
                      "string"
                    ],
                    "mmsi": [
                      "string"
                    ],
                    "name": [
                      "Ava Chen"
                    ],
                    "pastFlags": [
                      "string"
                    ],
                    "programId": [
                      "string"
                    ],
                    "sourceUrl": [
                      "https://example.com"
                    ],
                    "topics": [
                      "string"
                    ],
                    "type": [
                      "string"
                    ]
                  },
                  "referents": [
                    "string"
                  ],
                  "schema": "string",
                  "target": true
                }
              ],
              "owner": [
                "string"
              ],
              "role": [
                "string"
              ]
            },
            "schema": "string",
            "target": true
          }
        ],
        "political": [
          "string"
        ],
        "position": [
          "string"
        ],
        "positionOccupancies": [
          {
            "caption": "string",
            "datasets": [
              "string"
            ],
            "firstSeen": "string",
            "id": "string",
            "lastChange": "string",
            "lastSeen": "string",
            "properties": {
              "holder": [
                "string"
              ],
              "post": [
                {
                  "caption": "string",
                  "datasets": [
                    "string"
                  ],
                  "firstSeen": "string",
                  "id": "string",
                  "lastChange": "string",
                  "lastSeen": "string",
                  "properties": {
                    "country": [
                      "string"
                    ],
                    "name": [
                      "Ava Chen"
                    ],
                    "topics": [
                      "string"
                    ]
                  },
                  "referents": [
                    "string"
                  ],
                  "schema": "string",
                  "target": true
                }
              ],
              "status": [
                "string"
              ]
            },
            "schema": "string",
            "target": true
          }
        ],
        "programId": [
          "string"
        ],
        "religion": [
          "string"
        ],
        "sanctions": [
          {
            "caption": "string",
            "datasets": [
              "string"
            ],
            "firstSeen": "string",
            "id": "string",
            "lastChange": "string",
            "lastSeen": "string",
            "properties": {
              "authority": [
                "string"
              ],
              "authorityId": [
                "string"
              ],
              "country": [
                "string"
              ],
              "entity": [
                "string"
              ],
              "listingDate": [
                "string"
              ],
              "program": [
                "string"
              ],
              "programId": [
                "string"
              ],
              "programUrl": [
                "https://example.com"
              ],
              "reason": [
                "string"
              ],
              "sourceUrl": [
                "https://example.com"
              ]
            },
            "schema": "string",
            "target": true
          }
        ],
        "sourceUrl": [
          "https://example.com"
        ],
        "taxNumber": [
          "string"
        ],
        "title": [
          "string"
        ],
        "topics": [
          "string"
        ],
        "uniqueEntityId": [
          "string"
        ],
        "unknownLinkFrom": [
          {
            "caption": "https://example.com",
            "datasets": [
              "https://example.com"
            ],
            "firstSeen": "https://example.com",
            "id": "https://example.com",
            "lastChange": "https://example.com",
            "lastSeen": "https://example.com",
            "properties": {
              "object": [
                "https://example.com"
              ],
              "role": [
                "https://example.com"
              ],
              "subject": [
                {
                  "caption": "https://example.com",
                  "datasets": [
                    "https://example.com"
                  ],
                  "firstSeen": "https://example.com",
                  "id": "https://example.com",
                  "lastChange": "https://example.com",
                  "lastSeen": "https://example.com",
                  "properties": {
                    "address": [
                      "https://example.com"
                    ],
                    "addressEntity": [
                      "https://example.com"
                    ],
                    "alias": [
                      "https://example.com"
                    ],
                    "birthCountry": [
                      "https://example.com"
                    ],
                    "birthDate": [
                      "https://example.com"
                    ],
                    "birthPlace": [
                      "https://example.com"
                    ],
                    "citizenship": [
                      "https://example.com"
                    ],
                    "country": [
                      "https://example.com"
                    ],
                    "createdAt": [
                      "https://example.com"
                    ],
                    "education": [
                      "https://example.com"
                    ],
                    "fatherName": [
                      "https://example.com"
                    ],
                    "firstName": [
                      "https://example.com"
                    ],
                    "gender": [
                      "https://example.com"
                    ],
                    "innCode": [
                      "https://example.com"
                    ],
                    "lastName": [
                      "https://example.com"
                    ],
                    "middleName": [
                      "https://example.com"
                    ],
                    "modifiedAt": [
                      "https://example.com"
                    ],
                    "name": [
                      "https://example.com"
                    ],
                    "nationality": [
                      "https://example.com"
                    ],
                    "notes": [
                      "https://example.com"
                    ],
                    "position": [
                      "https://example.com"
                    ],
                    "programId": [
                      "https://example.com"
                    ],
                    "sourceUrl": [
                      "https://example.com"
                    ],
                    "topics": [
                      "https://example.com"
                    ],
                    "uniqueEntityId": [
                      "https://example.com"
                    ],
                    "wikidataId": [
                      "https://example.com"
                    ],
                    "wikipediaUrl": [
                      "https://example.com"
                    ]
                  },
                  "referents": [
                    "https://example.com"
                  ],
                  "schema": "https://example.com",
                  "target": true
                }
              ]
            },
            "schema": "https://example.com",
            "target": true
          }
        ],
        "unknownLinkTo": [
          {
            "caption": "https://example.com",
            "datasets": [
              "https://example.com"
            ],
            "firstSeen": "https://example.com",
            "id": "https://example.com",
            "lastChange": "https://example.com",
            "lastSeen": "https://example.com",
            "properties": {
              "object": [
                {
                  "caption": "https://example.com",
                  "datasets": [
                    "https://example.com"
                  ],
                  "firstSeen": "https://example.com",
                  "id": "https://example.com",
                  "lastChange": "https://example.com",
                  "lastSeen": "https://example.com",
                  "properties": {
                    "country": [
                      "https://example.com"
                    ],
                    "name": [
                      "https://example.com"
                    ],
                    "registrationNumber": [
                      "https://example.com"
                    ],
                    "topics": [
                      "https://example.com"
                    ]
                  },
                  "schema": "https://example.com",
                  "target": true
                }
              ],
              "role": [
                "https://example.com"
              ],
              "subject": [
                "https://example.com"
              ]
            },
            "schema": "https://example.com",
            "target": true
          }
        ],
        "weakAlias": [
          "string"
        ],
        "website": [
          "string"
        ],
        "wikidataId": [
          "string"
        ],
        "wikipediaUrl": [
          "https://example.com"
        ]
      },
      "referents": [
        "string"
      ],
      "schema": "string",
      "target": true
    }
  ],
  "meta": {}
}
```

See the full [Get Entity action reference](actions/get-entity.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/openSanctions/latest/actions/get-entity).
