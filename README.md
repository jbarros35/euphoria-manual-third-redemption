# Euphoria Third Redemption

## Third redemption data

- Number of addresses that redeemed during the second phase: 256 + 3 addresses for testing = 259 addresses in total that can redeem during the third phase.
- Total remaining assets (USDC): 2,135,244.728 USDC - 100 USDC (safety margin for math + testing) = 2,135,144.728 USDC
- Total redeemable wsWAGMI: 18,688.593054586418086809
- Redemption rate per wsWAGMI for the third phase: $114.249 per wsWAGMI

## Redemption instructions using Avalanche's Snowtrace Explorer:

1. You need AVAX in your wallet in order to interact with the redemption contract. You can purchase AVAX on most CEX:es.

2. To interact with the contract you usually only need a couple of cents worth of AVAX, but we recommend funding your wallet with at least 0.05 AVAX to perform the redemption and then having sufficient AVAX for gas to send the native USDC to a CEX or performing additional onchain activities.

3. Open the [claims.json](https://raw.githubusercontent.com/VenomProtocol/euphoria-manual-third-redemption/main/claims.json) file in a separate tab/window and search for your wallet address.

4. Pay attention to the `"amountIn"`, `"account"`, `"amount"`, and `"merkleProof"` variables and their respective values next your address / within the same surrounding `{}` block. You will need these values for the next steps.

5. [Open the redemption contract on Snowtrace](https://snowtrace.io/address/0x6155Fa6C11f42309C775F6a9eb997D2c16E423D6#writeContract) in a separate tab or window.

6. Click on `"2. exchangeForAssets"`

7. Now enter the values for the `"amountIn"`, `"account"`, `"amount"`, and `"merkleProof"` variables that matches your wallet in [claims.json](https://raw.githubusercontent.com/VenomProtocol/euphoria-manual-third-redemption/main/claims.json). **IMPORTANT: Enter the values without quotes.**

8. For the `"merkleProof"` field, start with a `[`, then combine the entire array/list into a single long string where every array/list member is separated by a comma, and finally end with a `]`. **IMPORTANT: Enter the values without quotes.**

9. Click on `"Write"`. If you haven't already connected your wallet of choice, connect it using the popup that pops up. Sign the transaction.

10. If the redemption was successful you should now have received native USDC in your wallet on Avalanche. You can add native USDC to your MetaMask by going to [TraderJoe](https://traderjoexyz.com/trade), selecting `"USDC"` as the `"To"` token, then clicking on the `"Add USDC to Wallet"` link below the `"Enter an amount"` button. You can also add it directly in MetaMask as a custom token using the contract address `0xB97EF9Ef8734C71904D8002F8b6Bc66Dd9c48a6E`.
