# brightcost-dashboard
[BrightCostDashboard.json](https://github.com/user-attachments/files/22531822/BrightCostDashboard.json)
{
  "properties": {
    "lenses": [
      {
        "order": 0,
        "parts": [
          {
            "position": {
              "x": 0,
              "y": 0,
              "colSpan": 7,
              "rowSpan": 5
            },
            "metadata": {
              "inputs": [
                {
                  "name": "ComponentId",
                  "value": "/subscriptions/1c21569c-d35c-4540-8958-ffca3f49471b/resourceGroups/rg-cost-optimizer/providers/Microsoft.OperationalInsights/workspaces/brightcost-logs",
                  "isOptional": true
                },
                {
                  "name": "TimeContext",
                  "value": null,
                  "isOptional": true
                },
                {
                  "name": "ResourceIds",
                  "value": [
                    "/subscriptions/1c21569c-d35c-4540-8958-ffca3f49471b/resourceGroups/rg-cost-optimizer/providers/Microsoft.OperationalInsights/workspaces/brightcost-logs"
                  ],
                  "isOptional": true
                },
                {
                  "name": "ConfigurationId",
                  "value": "/subscriptions/1c21569c-d35c-4540-8958-ffca3f49471b/resourcegroups/rg-cost-optimizer/providers/microsoft.insights/workbooks/64e11eb9-286a-4784-a5b3-4b23f59b3046",
                  "isOptional": true
                },
                {
                  "name": "Type",
                  "value": "workbook",
                  "isOptional": true
                },
                {
                  "name": "GalleryResourceType",
                  "value": "microsoft.operationalinsights/workspaces",
                  "isOptional": true
                },
                {
                  "name": "PinName",
                  "value": "BrightCost Dashboard",
                  "isOptional": true
                },
                {
                  "name": "StepSettings",
                  "value": "{\"version\":\"KqlItem/1.0\",\"query\":\"StorageBlobLogs\\n| where AccountName == \\\"brightcoststorage\\\"\\n| summarize Reads = countif(OperationName == \\\"GetBlob\\\"), \\n            Writes = countif(OperationName == \\\"PutBlob\\\")\\n            by bin(TimeGenerated, 1h)\\n| order by TimeGenerated desc\\n\",\"size\":0,\"timeContext\":{\"durationMs\":86400000},\"queryType\":0,\"resourceType\":\"microsoft.operationalinsights/workspaces\",\"visualization\":\"linechart\",\"sortBy\":[]}",
                  "isOptional": true
                },
                {
                  "name": "ParameterValues",
                  "value": {},
                  "isOptional": true
                },
                {
                  "name": "Location",
                  "value": "eastus",
                  "isOptional": true
                }
              ],
              "type": "Extension/AppInsightsExtension/PartType/PinnedNotebookQueryPart"
            }
          },
          {
            "position": {
              "x": 7,
              "y": 0,
              "colSpan": 6,
              "rowSpan": 4
            },
            "metadata": {
              "inputs": [
                {
                  "name": "ComponentId",
                  "value": "/subscriptions/1c21569c-d35c-4540-8958-ffca3f49471b/resourceGroups/rg-cost-optimizer/providers/Microsoft.OperationalInsights/workspaces/brightcost-logs",
                  "isOptional": true
                },
                {
                  "name": "TimeContext",
                  "value": null,
                  "isOptional": true
                },
                {
                  "name": "ResourceIds",
                  "value": [
                    "/subscriptions/1c21569c-d35c-4540-8958-ffca3f49471b/resourceGroups/rg-cost-optimizer/providers/Microsoft.OperationalInsights/workspaces/brightcost-logs"
                  ],
                  "isOptional": true
                },
                {
                  "name": "ConfigurationId",
                  "value": "/subscriptions/1c21569c-d35c-4540-8958-ffca3f49471b/resourcegroups/rg-cost-optimizer/providers/microsoft.insights/workbooks/64e11eb9-286a-4784-a5b3-4b23f59b3046",
                  "isOptional": true
                },
                {
                  "name": "Type",
                  "value": "workbook",
                  "isOptional": true
                },
                {
                  "name": "GalleryResourceType",
                  "value": "microsoft.operationalinsights/workspaces",
                  "isOptional": true
                },
                {
                  "name": "PinName",
                  "value": "BrightCost Dashboard",
                  "isOptional": true
                },
                {
                  "name": "StepSettings",
                  "value": "{\"version\":\"KqlItem/1.0\",\"query\":\"StorageBlobLogs\\n| where AccountName == \\\"brightcoststorage\\\"\\n| extend StatusCodeInt = toint(StatusCode)   // convert string → int\\n| where StatusCodeInt >= 400\\n| summarize FailedRequests = count() by bin(TimeGenerated, 1h)\\n| order by TimeGenerated desc\\n\",\"size\":0,\"timeContext\":{\"durationMs\":86400000},\"queryType\":0,\"resourceType\":\"microsoft.operationalinsights/workspaces\",\"visualization\":\"barchart\"}",
                  "isOptional": true
                },
                {
                  "name": "ParameterValues",
                  "value": {},
                  "isOptional": true
                },
                {
                  "name": "Location",
                  "value": "eastus",
                  "isOptional": true
                }
              ],
              "type": "Extension/AppInsightsExtension/PartType/PinnedNotebookQueryPart"
            }
          },
          {
            "position": {
              "x": 7,
              "y": 4,
              "colSpan": 6,
              "rowSpan": 4
            },
            "metadata": {
              "inputs": [
                {
                  "name": "ComponentId",
                  "value": "/subscriptions/1c21569c-d35c-4540-8958-ffca3f49471b/resourceGroups/rg-cost-optimizer/providers/Microsoft.OperationalInsights/workspaces/brightcost-logs",
                  "isOptional": true
                },
                {
                  "name": "TimeContext",
                  "value": null,
                  "isOptional": true
                },
                {
                  "name": "ResourceIds",
                  "value": [
                    "/subscriptions/1c21569c-d35c-4540-8958-ffca3f49471b/resourceGroups/rg-cost-optimizer/providers/Microsoft.OperationalInsights/workspaces/brightcost-logs"
                  ],
                  "isOptional": true
                },
                {
                  "name": "ConfigurationId",
                  "value": "/subscriptions/1c21569c-d35c-4540-8958-ffca3f49471b/resourcegroups/rg-cost-optimizer/providers/microsoft.insights/workbooks/64e11eb9-286a-4784-a5b3-4b23f59b3046",
                  "isOptional": true
                },
                {
                  "name": "Type",
                  "value": "workbook",
                  "isOptional": true
                },
                {
                  "name": "GalleryResourceType",
                  "value": "microsoft.operationalinsights/workspaces",
                  "isOptional": true
                },
                {
                  "name": "PinName",
                  "value": "BrightCost Dashboard",
                  "isOptional": true
                },
                {
                  "name": "StepSettings",
                  "value": "{\"version\":\"KqlItem/1.0\",\"query\":\"StorageBlobLogs\\n| where AccountName == \\\"brightcoststorage\\\"\\n| summarize Count = count() by OperationName\\n| order by Count desc\\n\",\"size\":0,\"timeContext\":{\"durationMs\":86400000},\"queryType\":0,\"resourceType\":\"microsoft.operationalinsights/workspaces\",\"visualization\":\"piechart\"}",
                  "isOptional": true
                },
                {
                  "name": "ParameterValues",
                  "value": {},
                  "isOptional": true
                },
                {
                  "name": "Location",
                  "value": "eastus",
                  "isOptional": true
                }
              ],
              "type": "Extension/AppInsightsExtension/PartType/PinnedNotebookQueryPart"
            }
          },
          {
            "position": {
              "x": 0,
              "y": 5,
              "colSpan": 7,
              "rowSpan": 4
            },
            "metadata": {
              "inputs": [
                {
                  "name": "ComponentId",
                  "value": "/subscriptions/1c21569c-d35c-4540-8958-ffca3f49471b/resourceGroups/rg-cost-optimizer/providers/Microsoft.OperationalInsights/workspaces/brightcost-logs",
                  "isOptional": true
                },
                {
                  "name": "TimeContext",
                  "value": null,
                  "isOptional": true
                },
                {
                  "name": "ResourceIds",
                  "value": [
                    "/subscriptions/1c21569c-d35c-4540-8958-ffca3f49471b/resourceGroups/rg-cost-optimizer/providers/Microsoft.OperationalInsights/workspaces/brightcost-logs"
                  ],
                  "isOptional": true
                },
                {
                  "name": "ConfigurationId",
                  "value": "/subscriptions/1c21569c-d35c-4540-8958-ffca3f49471b/resourcegroups/rg-cost-optimizer/providers/microsoft.insights/workbooks/64e11eb9-286a-4784-a5b3-4b23f59b3046",
                  "isOptional": true
                },
                {
                  "name": "Type",
                  "value": "workbook",
                  "isOptional": true
                },
                {
                  "name": "GalleryResourceType",
                  "value": "microsoft.operationalinsights/workspaces",
                  "isOptional": true
                },
                {
                  "name": "PinName",
                  "value": "BrightCost Dashboard",
                  "isOptional": true
                },
                {
                  "name": "StepSettings",
                  "value": "{\"version\":\"KqlItem/1.0\",\"query\":\"StorageBlobLogs\\n| where AccountName == \\\"brightcoststorage\\\"\\n| summarize Ingress = sum(RequestBodySize), \\n            Egress = sum(ResponseBodySize)\\n            by bin(TimeGenerated, 1h)\\n| order by TimeGenerated desc\\n\",\"size\":0,\"timeContext\":{\"durationMs\":86400000},\"queryType\":0,\"resourceType\":\"microsoft.operationalinsights/workspaces\",\"visualization\":\"areachart\"}",
                  "isOptional": true
                },
                {
                  "name": "ParameterValues",
                  "value": {},
                  "isOptional": true
                },
                {
                  "name": "Location",
                  "value": "eastus",
                  "isOptional": true
                }
              ],
              "type": "Extension/AppInsightsExtension/PartType/PinnedNotebookQueryPart"
            }
          }
        ]
      }
    ],
    "metadata": {
      "model": {
        "timeRange": {
          "value": {
            "relative": {
              "duration": 24,
              "timeUnit": 1
            }
          },
          "type": "MsPortalFx.Composition.Configuration.ValueTypes.TimeRange"
        },
        "filterLocale": {
          "value": "en-us"
        },
        "filters": {
          "value": {
            "MsPortalFx_TimeRange": {
              "model": {
                "format": "utc",
                "granularity": "auto",
                "relative": "24h"
              },
              "displayCache": {
                "name": "UTC Time",
                "value": "Past 24 hours"
              },
              "filteredPartIds": [
                "StartboardPart-PinnedNotebookQueryPart-a54f834a-ebc3-4cec-a09d-76d7f87718dc",
                "StartboardPart-PinnedNotebookQueryPart-a54f834a-ebc3-4cec-a09d-76d7f87718de",
                "StartboardPart-PinnedNotebookQueryPart-a54f834a-ebc3-4cec-a09d-76d7f87718e0",
                "StartboardPart-PinnedNotebookQueryPart-a54f834a-ebc3-4cec-a09d-76d7f87718e2"
              ]
            }
          }
        }
      }
    }
  },
  "name": "BrightCostDashboard",
  "type": "Microsoft.Portal/dashboards",
  "location": "INSERT LOCATION",
  "tags": {
    "hidden-title": "BrightCostDashboard"
  },
  "apiVersion": "2022-12-01-preview"
}
