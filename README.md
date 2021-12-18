# strategy
This strategy simply deposits btc into [ribbon's covered call strategy](https://www.ribbon.finance/) to earn yield(premium from selling options). 

It imitates creating our own covered call strategy which could be done easily with [opyn's perpetual vault template](https://github.com/opynfinance/perp-vault-templates/blob/master/contracts/example-actions/ShortOToken.sol). The covered call strategy involves depositing btc as collateral into opyn vault and shorting btc call options (same with ribbon).

Due to the nature of withdrawals from the ribbon vault, the following function inplementations were changed to enable our strategy to remain compatible with badger:

`_withdrawSome(amount)` -> This initiates a withdrawal from the ribbon vault which could be completed later in the future

`_withdrawAll()` ->  This completes an already initiated withdrawal from ribbon vault.


# todo
- do more research
- write tests for current strategy
- do a similiar strategy for [stakedao]()


# helpful links
- https://www.opyn.co
- https://www.ribbon.finance
- https://stakedao.org/
