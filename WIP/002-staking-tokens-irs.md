This document is still in draft WIP mode.

---

The IRS currently treats all staking rewards as income when received, but this
stance poses an existential threat to crypto.

Separation of token from consensus is not a new concept for crypto. The first
and still the top blockchain project, Bitcoin, utilizes proof-of-work for its
consensus, whereas the BTC bitcoin tokens are not used directly for mining.
This is a feature of its security, because energy is abundant (especially
equally from the sun), and efficient Bitcoin mining is a highly technical
endeavor, whereas the purpose of BTC is for payments among the general
population who are luddites in comparison to Bitcoin miners.

The Cosmos whitepaper came out in 2017 and became a sensation because it was
the first to provably solve the "nothing at stake" problem of prior
proof-of-stake solutions; Cosmos made proof-of-stake a theoretically sound
alternative to proof-of-work. We now have a revived Byzantine Fault Tolerance
research and implementation industry and about ten thousand unique blockchains
partially thanks to the innovations of Cosmos and Tendermint.

In Cosmos, and in its fork AtomOne, the staking token (ATOM and ATONE
respectively) are designed to be largely staked, targetting a massive staking
ratio of 2/3, or 67%. It is the first provably secure BFT proof-of-stake
system, and it also targets the highest staking ratio. And the ATOM token was
since the very beggining, pitched as a "staking token" separate in class than
those of other utility tokens. The Cosmos whitepaper describes a dual-token
model where the ATOM token is the staking token, and other tokens in the Cosmos
hub can function as the secondary fee token. The AtomOne blockchain forks
Cosmos and provides a specific secondary fee token PHOTON to complement the
staking token ATONE.

Ethereum converted from proof-of-work to proof-of-stake in the year XXX and
doesn't target a specific staking ratio, but uses a formula to determine the
staking inflation rate to incentivize staking. Its staking ratio has settled to
about 27%. Unlike Bitcoin or Cosmos, Ethereum uses the same token for both fee
payments as well as staking for consensus.

Cosmos's dual token model has real benefits over Ethereum's single token model.
The staking token distribution can be different than the fee token
distribution, allowing different expectations and incentives. For example, the
slashing function of proof-of-stake (for validators that misbehave) only apply
to stakers, whereas non-stakers who only hold fee tokens need not be concerned
about the risks of slashing. For the most innovation in proof-of-stake
dual-token design, see the AtomOne constitution which provides limitations of
inflation for the fee token holder with the PHOTON fee token.

Another benefit of the dual-token model is the preservation of sovereignty of
the technical core creators and supporters. In a single-token proof of stake
blockchain like Ethereum there is a well defined cost to taking over the
consensus security of the chain and having complete control over the
blockchain. There is a fixed cost to any whale capital investor who accumulates
enough voting stake to take control of the chain and even attack it. In
contrast in a dual token model the blockchain can only lose control to capital
investors (potentially hostile) if the stakers choose to sell their stake. Thus
for example if TexasChain created by the State of Texas wanted to issue
gold-backed tokens to foreign investors without losing control of TexasChain to
foreign powers, it must employ a dual-token model.

Another analogy to convince the reader about the merits of the dual token model
can be found in the design of shareholder companies of general partners. Such a
company would naturally want to rely on the expertise and insights of the
general partners for the execution of its business, which for example might
involve the sale of computers like Apple does, or Beanie Babies for a more
fungible example. Whereas if the company were controlled by the customers, it
probably would not have been as successful. “If I had asked people what they
wanted, they would have said faster horses.” (commonly attributed to Ford).

Whether the proof of stake chain employes a single token model or dual token
model for its staking security, there is a spectrum of them where the
distinguishing variable is the ratio of total tokens staked.

If the staking ratio is very high, the staking economics acts more like a
penalty for those who don't stake.  When the staking ratio is the highest at
100%, there is in effect no income, because all inflation are distributed
pro-rata to the stakers with no change in distribution before and after the
staking reward.

If the staking ratio is very low, the staking economics acts more like a reward
for those who do stake. When the staking ratio is for example at a low 0.1%, it
is in effect income, because there is a tax upon the non-stakers and the
proceeds are distributed to the stakers, reflected as change in the
distribution.

Furthermore, single token proof-of-stake chains can only tolerate a low
inflation rate (because the targetted class of token users are not stakers),
whereas dual-token proof-of-stake chains target a higher staking rate for its
security (sovereignty) and to incentivize the distinction into being -- that
is, to dissuade the lay crypto user from participating in staking (with risk of
slashing).

In the Tezos appeal case [XXX link to] the court published a preliminary
response that denies Tezos stakers favorable tax treatment (and instead that
earned staking inflation should be counted as income upon the receipt, rather
than the sale of those tokens). The basis of this is that the IRS denies that
the Tezos stakers have "created" the newly minted staking tokens. The IRS did
not state why, merely denying the plaintiff's claims.

This preliminary conclusion might be acceptable if the staking ratio for a
proof-of-stake blockchain is low, because most of the staking inflation reward
distribution corresponds to a transfer from non-stakers to stakers, and vice
versa when the staking ratio is high, less of the staking inflation reward
distribution corresponds to such a transfer. For clarification, if staking
rewards were like farmers' chickens laying baby chicks, a low staking ratio is
like chicken farmers globally paying taxes in the form of hatched chicks to the
few staking farmers for the service of staking; where a high staking ratio
means most of the hated chicks distributed were paid back to the farmer that
actually created them. To see how the math is skewed unreasonably against the
high staking ratio farmer, see the blog post ["Atom Must Not Be Money"](https://allinbits.com/blog/nwv-to-prop-848-atom-must-not-be-money/) which
shows that for a 30% annual staking reward, 8.33% corresponds to a transfer
from non-stakers, whereas a whopping (30 - 8.33) = 21.67% corresponds to self
creation, which is 72.22% of the total rewards.

This makes the IRS's position on staking reward taxation not only unfair for
blockchains that have or target high staking ratios; it makes them ecomically
infeasible. Even in a state of stasis with no other economic activity, the IRS
through taxes would end up taking the vast majority of a Cosmso or AtomOne
staker's net ownership of staking tokens in a matter of decades. And given that
dual-token proof of stake chains target a high inflation rate, the IRS is
effectively enforcing illegal sanctions on a whole class of sovereign crypto
and forcing all crypto to be vulnerable to takeover from capital investors.
Not even going public in the seurities markets enforces such a thing.  The IRS
should not use its taxing authority to stifle home grown innovation in the
crypto blockchain space.

Whether or not staking inflation rewards are considered taxable upon reward as
income or taxable upon later sale under capital gains/loss treatment, we
recommend that the IRS create a special class of crypto tokens called "staking
tokens" that is only taxed upon sale of the inflated staking tokens earned by
stakers; given that the staking ratio targetted is greater than 50%, and during
the periods where the actual staking ratio is greater than 50%. This will allow
secure proof-of-stake blockchains to exist within the frame of US tax law,
ensuring that the US can continue to innovate in secure proof-of-stake chains
and participate in their staking security.

---


* internally in implementation when somebody stakes, atoms are converted to a
  non transferable token called something else. This value is such that it does
  not change in quantity after staking even after years, unless slashing is
  applied. For example, 1M atoms staked becomes 1K shares (say). After years
  with no slashing one still has 1K shares, and only when unbonding does the
  shares become say, 2M atoms. If we considered these internal representations
  the tax result would be I believe more favorable — at least capital gains,
  and only upon unbonding. But this still isn’t fair.

* staking token inflation rewards should be distinguished from tx priority fee
  distribution rewards. The latter really is income. This recommendation only
  pertains to the staking rewards that are not derived from transaction fees.

* even without IRS clarification as recommended here, developers of
  proof-of-stake blockchains can make a trivial change to make the total amount
  of staked tokens remain the same, while reducing the amount of non-staked
  tokens in non-staked accounts by introducing a global denominator.  This
  mental exercise and real potential workaround demonstrates the illogical
  nature of the IRS's current position that all staking tokens are to be
  treated as income.

 * see also https://allinbits.com/blog/nwv-to-prop-848-atom-must-not-be-money/


-- All in Bits, Inc 
