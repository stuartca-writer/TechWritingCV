---
description: Below is an example of an API that I wrote.
---

# API example

### SKU Placements resource <a href="#_70tc4vr692i5" id="_70tc4vr692i5"></a>

| Version              | 1                                                                                                                    |
| -------------------- | -------------------------------------------------------------------------------------------------------------------- |
| Base URL             | https://api.\[...]                                                                                                   |
| Service account role | WS Store layout                                                                                                      |
| Sandbox mocks        | [Yes](https://help.abundo.osp.tech/en-us/developer/api/sandbox/scenarios/store-pick)                                 |
| Swagger available    | [Download Swagger](https://help.abundo.osp.tech/api/sku-placements-1.json)                                           |
| Endpoint reference   | [SKU Placements resource](https://help.abundo.osp.tech/en-us/developer/api/reference/isf/sku-placements/1/reference) |
| Status               | Active                                                                                                               |

Use the SKU placements resource to view, create, update, and delete the placement of products in one of your stores.

The SKU placements resource is just one of the resources you need to use when managing a store-picking operation. See [Using APIs to configure In-Store Fulfillment](https://help.abundo.osp.tech/en-us/developer/api/reference/isf/using-isf-apis) to find out more about these resources, and how to use them.

### Understanding SKU placements <a href="#_h5iuc28jpk0c" id="_h5iuc28jpk0c"></a>

To enable a product to be picked in one of your stores, the store-picking application displays the required SKU to the picker, along with its expected location. This helps to direct pickers to the correct location, and to ensure the most efficient pick walk around the store.

This information - where the SKU is expected to be - is called a SKU placement. It is a mapping between a SKU and a [pick location](https://help.abundo.osp.tech/en-us/developer/api/reference/isf/pick-locations/).

Updates that have passed their finalization time will not be reflected in the shipments. Example: If Shipment A has a finalization time of midnight and Shipment B has a finalization time of 15:00, if the user updates locations at 10am the changes will not occur for shipment A, but they will for shipment B.\\

### In-Store Fulfillment resource scenarios <a href="#_xr89q1qpmmmd" id="_xr89q1qpmmmd"></a>

This page contains some sample API calls and responses that you can make with the In-Store Fulfillment resources, using the sandbox environment.

[See the full API reference for the Pick Locations resource](https://help.abundo.osp.tech/en-us/developer/api/reference/isf/pick-locations/).

[See the full API reference for the SKU Placements resource](https://help.abundo.osp.tech/en-us/developer/api/reference/isf/sku-placements/).

### Scenarios <a href="#_jjd8vbimp824" id="_jjd8vbimp824"></a>

[Get SKU placements](https://help.abundo.osp.tech/en-us/developer/api/sandbox/scenarios/store-pick#endpoint-1-get-sku-placements)

GET /v1/sites/{retailerSiteId}/sku-placements

### Get SKU placements <a href="#_8a7o2xrsfnwj" id="_8a7o2xrsfnwj"></a>

[Success](https://help.abundo.osp.tech/en-us/developer/api/sandbox/scenarios/store-pick#scenario-1-success)

GET /v1/sites/65536661/sku-placements?retailerSkuId=75334667\&pickLocationId=59304427\&maxPageSize=5\&pageToken=7b5e1d74-aec7-4671-a175-5ba0ae38ed89

**Success**

| GET                                                                                                                                                                                                                                                                                                                                                                                              | /v1/sites/65536661/sku-placements?retailerSkuId=75334667\&pickLocationId=59304427\&maxPageSize=5\&pageToken=7b5e1d74-aec7-4671-a175-5ba0ae38ed89 |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| Response                                                                                                                                                                                                                                                                                                                                                                                         |                                                                                                                                                  |
| <p>Status code: 200</p><p>{</p><p>"metadata": {</p><p>"nextPageToken": "7b5e1d74-aec7-4671-a175-5ba0ae38ed89",</p><p>"pageToken": "7b5e1d74-aec7-4671-a175-5ba0ae38ed89",</p><p>"maxPageSize": 20</p><p>},</p><p>"content": [</p><p>{</p><p>"pickLocationId": "59304427",</p><p>"priority": 1,</p><p>"retailerSkuId": "75334667",</p><p>"skuPlacementId": "30593308"</p><p>}</p><p>]</p><p>}</p> |                                                                                                                                                  |
