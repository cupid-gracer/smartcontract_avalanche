//////////////airdrop.sol
no settings after deploy

//////////////locker.sol
default fee 1 avax changable
default company wallet 0x0

should set company wallet after deploy

//////////////snow-burn.sol        need to test again
default marketing address           0xf17f39713A04349737dfF451Fa2c571229945b70 changable
name Snow                           burn
symbol                              BURN
decimals                            18
tax fee                             3 //distribution
liquidity and marketing fee         12
marketingdivisor                    8 //means 8 for marketing, 4(12 - 8) for liquidity
max tx amount                       10 ^ 11
maxlimit                            2 ^ 10 // wallet can hold token max this amount
minimum for swap                    10 ^ 6 // distribute occures more than this value
min for top level holder            2 ^ 8
router                              0x60aE616a2155Ee3d9A68541Ba4544862310933d4 // trader joe

exclude from fee                    owner, this contract // changable
exclude from whale                  owner, this contract, deadaddress, marketingaddress, uniswapv2pair
swap and liquidify                  false
oneToOneBurn                        false

functions////////////////
initialize            make router, pair to exclude from whale
setDynamicFee         set dynamic fee only for sell(only for trader joe) 25% - 15% for one day
preparingForBeforePresale   fee to 0    max tx amount 10 ^ 12
afterPresale                tax to 4, liquidityandmarketing to 11, max tx amount to 10 ^ 11


/////////////vesting
feesInETH 1avax changable
companyWallet 0x0 changable

need to set companywallet after deploy