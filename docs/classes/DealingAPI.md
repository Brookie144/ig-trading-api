[ig-trading-api](../README.md) / [Exports](../modules.md) / DealingAPI

# Class: DealingAPI

## Table of contents

### Constructors

- [constructor](DealingAPI.md#constructor)

### Properties

- [URL](DealingAPI.md#url)

### Methods

- [closePosition](DealingAPI.md#closeposition)
- [confirmTrade](DealingAPI.md#confirmtrade)
- [createOrder](DealingAPI.md#createorder)
- [createPosition](DealingAPI.md#createposition)
- [deleteOrder](DealingAPI.md#deleteorder)
- [getAllOpenPositions](DealingAPI.md#getallopenpositions)
- [getAllOrders](DealingAPI.md#getallorders)
- [getPosition](DealingAPI.md#getposition)
- [updateOrder](DealingAPI.md#updateorder)
- [updatePosition](DealingAPI.md#updateposition)

## Constructors

### constructor

• **new DealingAPI**(`apiClient`)

#### Parameters

| Name        | Type            |
| :---------- | :-------------- |
| `apiClient` | `AxiosInstance` |

#### Defined in

[dealing/DealingAPI.ts:213](https://github.com/bennycode/ig-trading-api/blob/c7d6810/src/dealing/DealingAPI.ts#L213)

## Properties

### URL

▪ `Static` `Readonly` **URL**: `Object`

#### Type declaration

| Name                | Type     |
| :------------------ | :------- |
| `CONFIRMS`          | `string` |
| `POSITIONS`         | `string` |
| `POSITIONS_OTC`     | `string` |
| `WORKINGORDERS`     | `string` |
| `WORKINGORDERS_OTC` | `string` |

#### Defined in

[dealing/DealingAPI.ts:205](https://github.com/bennycode/ig-trading-api/blob/c7d6810/src/dealing/DealingAPI.ts#L205)

## Methods

### closePosition

▸ **closePosition**(`closePositionRequest`): `Promise`<[`DealReferenceResponse`](../interfaces/DealReferenceResponse.md)\>

Closes an OTC position.

**`see`** https://labs.ig.com/rest-trading-api-reference/service-detail?id=542

#### Parameters

| Name                   | Type                                                            |
| :--------------------- | :-------------------------------------------------------------- |
| `closePositionRequest` | [`PositionCloseRequest`](../interfaces/PositionCloseRequest.md) |

#### Returns

`Promise`<[`DealReferenceResponse`](../interfaces/DealReferenceResponse.md)\>

#### Defined in

[dealing/DealingAPI.ts:267](https://github.com/bennycode/ig-trading-api/blob/c7d6810/src/dealing/DealingAPI.ts#L267)

---

### confirmTrade

▸ **confirmTrade**(`dealReference`): `Promise`<[`DealConfirmation`](../interfaces/DealConfirmation.md)\>

Returns a deal confirmation for the given deal reference.

**`see`** https://labs.ig.com/rest-trading-api-reference/service-detail?id=546

#### Parameters

| Name | Type | Description |
| :-- | :-- | :-- |
| `dealReference` | [`DealReferenceResponse`](../interfaces/DealReferenceResponse.md) | The dealReference of the deal to be retrieved |

#### Returns

`Promise`<[`DealConfirmation`](../interfaces/DealConfirmation.md)\>

#### Defined in

[dealing/DealingAPI.ts:299](https://github.com/bennycode/ig-trading-api/blob/c7d6810/src/dealing/DealingAPI.ts#L299)

---

### createOrder

▸ **createOrder**(`createOrderRequest`): `Promise`<[`DealReferenceResponse`](../interfaces/DealReferenceResponse.md)\>

Creates an OTC working order.

**`see`** https://labs.ig.com/rest-trading-api-reference/service-detail?id=533

#### Parameters

| Name                 | Type                                                        |
| :------------------- | :---------------------------------------------------------- |
| `createOrderRequest` | [`OrderCreateRequest`](../interfaces/OrderCreateRequest.md) |

#### Returns

`Promise`<[`DealReferenceResponse`](../interfaces/DealReferenceResponse.md)\>

#### Defined in

[dealing/DealingAPI.ts:326](https://github.com/bennycode/ig-trading-api/blob/c7d6810/src/dealing/DealingAPI.ts#L326)

---

### createPosition

▸ **createPosition**(`createPositionRequest`): `Promise`<[`DealReferenceResponse`](../interfaces/DealReferenceResponse.md)\>

Creates an OTC position.

**`see`** https://labs.ig.com/rest-trading-api-reference/service-detail?id=542

#### Parameters

| Name                    | Type                                                              |
| :---------------------- | :---------------------------------------------------------------- |
| `createPositionRequest` | [`PositionCreateRequest`](../interfaces/PositionCreateRequest.md) |

#### Returns

`Promise`<[`DealReferenceResponse`](../interfaces/DealReferenceResponse.md)\>

#### Defined in

[dealing/DealingAPI.ts:251](https://github.com/bennycode/ig-trading-api/blob/c7d6810/src/dealing/DealingAPI.ts#L251)

---

### deleteOrder

▸ **deleteOrder**(`dealId`): `Promise`<[`DealReferenceResponse`](../interfaces/DealReferenceResponse.md)\>

Deletes an OTC working order.

**`see`** https://labs.ig.com/rest-trading-api-reference/service-detail?id=526

#### Parameters

| Name     | Type     |
| :------- | :------- |
| `dealId` | `String` |

#### Returns

`Promise`<[`DealReferenceResponse`](../interfaces/DealReferenceResponse.md)\>

#### Defined in

[dealing/DealingAPI.ts:342](https://github.com/bennycode/ig-trading-api/blob/c7d6810/src/dealing/DealingAPI.ts#L342)

---

### getAllOpenPositions

▸ **getAllOpenPositions**(): `Promise`<[`PositionListResponse`](../interfaces/PositionListResponse.md)\>

Returns all open positions for the active account.

**`see`** https://labs.ig.com/rest-trading-api-reference/service-detail?id=545

#### Returns

`Promise`<[`PositionListResponse`](../interfaces/PositionListResponse.md)\>

#### Defined in

[dealing/DealingAPI.ts:220](https://github.com/bennycode/ig-trading-api/blob/c7d6810/src/dealing/DealingAPI.ts#L220)

---

### getAllOrders

▸ **getAllOrders**(): `Promise`<[`OrderListResponse`](../interfaces/OrderListResponse.md)\>

Returns all open working orders for the active account.

**`see`** https://labs.ig.com/rest-trading-api-reference/service-detail?id=555

#### Returns

`Promise`<[`OrderListResponse`](../interfaces/OrderListResponse.md)\>

#### Defined in

[dealing/DealingAPI.ts:310](https://github.com/bennycode/ig-trading-api/blob/c7d6810/src/dealing/DealingAPI.ts#L310)

---

### getPosition

▸ **getPosition**(`dealId`): `Promise`<[`Position`](../interfaces/Position.md)\>

Returns an open position for the active account by deal identifier.

**`see`** https://labs.ig.com/rest-trading-api-reference/service-detail?id=541

#### Parameters

| Name     | Type     |
| :------- | :------- |
| `dealId` | `String` |

#### Returns

`Promise`<[`Position`](../interfaces/Position.md)\>

#### Defined in

[dealing/DealingAPI.ts:235](https://github.com/bennycode/ig-trading-api/blob/c7d6810/src/dealing/DealingAPI.ts#L235)

---

### updateOrder

▸ **updateOrder**(`dealId`, `orderRequest`): `Promise`<[`DealReferenceResponse`](../interfaces/DealReferenceResponse.md)\>

Updates an OTC working order.

**`see`** https://labs.ig.com/rest-trading-api-reference/service-detail?id=526

#### Parameters

| Name           | Type                                                        |
| :------------- | :---------------------------------------------------------- |
| `dealId`       | `String`                                                    |
| `orderRequest` | [`OrderUpdateRequest`](../interfaces/OrderUpdateRequest.md) |

#### Returns

`Promise`<[`DealReferenceResponse`](../interfaces/DealReferenceResponse.md)\>

#### Defined in

[dealing/DealingAPI.ts:364](https://github.com/bennycode/ig-trading-api/blob/c7d6810/src/dealing/DealingAPI.ts#L364)

---

### updatePosition

▸ **updatePosition**(`dealId`, `updatePositionRequest`): `Promise`<[`DealReferenceResponse`](../interfaces/DealReferenceResponse.md)\>

Updates an OTC position.

**`see`** https://labs.ig.com/rest-trading-api-reference/service-detail?id=542

#### Parameters

| Name                    | Type                                                              |
| :---------------------- | :---------------------------------------------------------------- |
| `dealId`                | `String`                                                          |
| `updatePositionRequest` | [`PositionUpdateRequest`](../interfaces/PositionUpdateRequest.md) |

#### Returns

`Promise`<[`DealReferenceResponse`](../interfaces/DealReferenceResponse.md)\>

#### Defined in

[dealing/DealingAPI.ts:283](https://github.com/bennycode/ig-trading-api/blob/c7d6810/src/dealing/DealingAPI.ts#L283)