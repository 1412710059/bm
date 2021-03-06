---
layout: default
title: Aprender acerca de los fondos de minería Bitcoin
description: Aprender acerca de los fondos de minería Bitcoin
toc:
  nc: Network Consensus
  bmp: Bitcoin Mining Pools
  hd: Hash Rate Distribution
  bmpo: Bitcoin Mining Pool Options
  pm: Bitcoin Mining Pool Payment Methods
---

{% include page-toc.html %}

<p>Bitcoin mining pools are a way for Bitcoin miners to pool their resources together and share their hashing power while splitting the reward equally according to the amount of shares they contributed to solving a block.</p>

<p>A "share" is awarded to members of the Bitcoin mining pool who present a valid <a href="/what-is-proof-of-work/">proof of work</a> that their Bitcoin miner solved. Bitcoin mining in pools began when the difficulty for mining increased to the point where it could take years for slower miners to generate a block.</p>

<p>The solution to this problem was for miners to pool their resources so they could generate blocks quicker and therefore receive a portion of the Bitcoin block reward on a consistent basis, rather than randomly once every few years.</p>

<h2 id="nc">Network Consensus</h2>

<center><img src="/images/bitcoin-network-consensus.jpg" alt="bitcoin network consensus"></center>

<p>If you solo-mine, meaning you do not mine with a Bitcoin mining pool, then you will need to ensure that you are in consensus with the Bitcoin network. The best way is to use the <a href="http://bitcoin.org/en/download">official BitCore client</a>.</p>

<p>If you participate in a Bitcoin mining pool then you will want to ensure that they are engaging in behavior that is in agreement with your philosophy towards Bitcoin.</p>

<p>For example, some rogue developers have threatened to release software that could hard-fork the network which would likely result in tremendous financial damage.</p>

<p>Therefore, it is your duty to make sure that any Bitcoin mining power you direct to a mining pool does not attempt to enforce network consensus rules you disagree with.</p>

<h2 id="bmp">Bitcoin Mining Pools</h2>

<p>There are many good Bitcoin mining pools to choose from. Although it's tempting to pick the most popular one, it's better for the health of the network to mine with smaller pools so as to avoid potentially harmful concentration of hashing power.</p>

<p>The hash rate distribution is best when split among more Bitcoin mining pools.</p>

<h2 id="hd">Bitcoin Mining Pool Hash Rate Distribution</h2>

<center><img src="/images/bitcoin-mining-pool-hash-rate-distribution.png"></center>

<h2 id="bmpo">Bitcoin Mining Pool Options</h2>

<p>For a fully decentralized pool, we highly recommend <a rel="nofollow" target="_blank" href="http://p2pool.in">p2pool</a>.</p>

<p>The following pools are believed to be <b>currently fully validating blocks</b> with Bitcoin Core 0.11 or later:</p>

{% for pool in site.data.pools %}
{% include pools.html %}
{% endfor %}

<h2 id="pm">Bitcoin Mining Pool Payment Methods</h2>

<p>Calculating your share of the bitcoins mined can be complex. In an ongoing effort to come up with the fairest method and prevent gaming of the system, many calculation schemes have been invented. The two most popular types are PPS and DGM. PPS, or 'pay per share' shifts the risk to the mining pool while they guarantee payment for every share you contribute.</p>

<p>PPS payment schemes require a very large reserve of 10,000 BTC in order to ensure they have the means of enduring a streak of bad luck. For this reason, most Bitcoin mining pools no longer support it.</p>

<p>One of the few remaining PPS pools is EclipseMC. DGM is a popular payment scheme because it offers a nice balance between short round and long round blocks.  However, end users must wait for full round confirmations long after the blocks are processed.</p>

{% for pp in site.data.pool-payouts %}
{% include pools-payouts.html %}
{% endfor %}
