## Change Log

### 1.12.23

- Uniformed options symbol construction (eg ``AAPL20161028P00115000``, ``SPX20161024P02150000``)
- Misc code improvements and minor bug fixes

### 1.12.22

- Misc code improvements and minor bug fixes

### 1.12.21

- Complete Options and Futures Options market data available via ``optionsData``

### 1.12.20

- Setting correct ``m_includeExpired`` for each asset class (solved a problem with historical data request not being acknowledged by TWS)

### 1.12.19

- Fixed some issues with stop limit and trailing stop orders

#### 1.12.18

- Fixed some issues with stop limit and trailing stop orders

#### 1.12.17

- Added flag for stop limit orders
- Misc code improvements and minor bug fixes

#### 1.12.16

- Misc code improvements and minor bug fixes

#### 1.12.15

- Misc code improvements and minor bug fixes

#### 1.12.14

- Callback now fires on TWS errors and and passes one of IB's [error codes](https://www.interactivebrokers.com/en/software/api/apiguide/tables/api_message_codes.htm).
- Callback fires upon lost connection to IB TWS/GW with the ``handleConnectionClosed`` event
- ``self.connected`` holds latest connection status (``True``/``False``)

#### 1.12.13

- Fixed bug that caused multiple ``clientId``s to be saved in the orderIds cache file. Now forcing saving of unique orderId in cache file.

#### 1.12.12

- ``cancelOrder()`` not requires ``orderId``
- Better hadling of canceled orders

#### 1.12.11

- Removed debugging code


#### 1.12.10

- Caching last ``orderId`` to keep a persistent ``orderId`` between TWS sessions (may require a one-time resetting of API Order ID Sequence, see
[https://www.interactivebrokers.com/en/software/csharp/topics/orders.htm](https://www.interactivebrokers.com/en/software/csharp/topics/orders.htm) for more information).


#### 1.12.9

- Calls ``requestPositionUpdates(...)`` and ``requestAccountUpdates(...)`` upon connecting by default
- Calls ``requestOrderIds()`` before every order submission to prevent conflicts with other programs submitting orders (other instances of ezIBpy included)

#### 1.12.8

- Renamed ``createFutureContract(...)`` to ``createFuturesContract(...)`` (old name still works for backward compatibility)

#### 1.12.7

- Changed default exhange to IDEALPRO in ``createCashContract(...)``
