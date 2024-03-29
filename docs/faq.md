# FAQ (Frequently Asked Questions)

## Using Rapid Transaction Propagation (RTP), can I save on gas fees and be the first at the same time?
With Front-Running your transaction will be picked and processed by Validators very fast, on average in some milliseconds. The next thing is how it will be prioritised in the order of the newest block globally.

Some Validators on the Ethereum chain, like Ethermine, use non-conventional ordering for their benefit, aka they generally don't do the by-gas sort. Other Validators can choose to sort by gas and nonce, others can choose to sort by gas and first-seen-time, others can first sort by gas and then randomise the order, others can sort by gas first and then put the "greatest" sender addresses at the top or bottom, which is converting an address to a 160-bit integer and working with those values.

If you’ll get to Validators first with calculated or higher gas, you can be more than sure you’ll get it. If there will be any other user with ZMOK’s PREMIUM plan, and you have a lower Gwei, there is a higher chance the other user will get the priority. Therefore we do not recommend lowering Gwei.
If you do not have PREMIUM plan, your transaction will be sent as a standard transaction to only one node, in only one region, and the chance that this transaction will be mined in the next block is lower, even if you’d use much higher gas.

## Is RTP necessary for minting NFTs?
Not really, a basic paid plan shall be enough.

## If current Gwei changes rapidly during the public drop, do I need to change my gas?
In this case, you must check on pending transactions, find one with the highest gast and after that submit again with the same nonce:
[How to send a replacement transaction with a higher gas price](https://ethereum.stackexchange.com/questions/99651/how-to-send-a-replacement-transaction-with-a-higher-gas-price?rq=1)

## What is the fastest way to communicate with ZMOK? WebSockets or HTTP?
If we'd need to decide between two variants (HTTP vs. WebSockets) in general, we'd prefer to recommend you the HTTP option. WS will connect you to only one node. It's cool if this node has your requested data already synced, so the answer will be fast. If not, this one node will wait to get data for you. For parsing new blocks, HTTP is highly recommended, because you're getting the answer from the cluster of nodes. This means the chance this will be the fastest way, for most of you, is much higher.

## Does my endpoint work?
You can do a very quick check by sending a curl request online with your endpoint, e.g. [https://reqbin.com/c-zokn0wuy](https://reqbin.com/c-zokn0wuy)
