# Part B: Design Document

**Marks:** 4 of 100 - the **Randomness** section below is read and marked. The
rest of this document is not scored, but it is read when we talk to you, so
answer it properly.

**Section 1: FreelanceBountyBoard**
**Section 2: DecentralisedRaffle**

Short, specific answers beat long vague ones. Three honest sentences score better
than a page of general security talk. If you ran out of time on something, say
so here - describing what you would have done still earns marks. Pretending it
is finished does not.

---

## WHY I BUILT IT THIS WAY

### 1. Data Structure Choices

- Where did you use a `mapping`, and where did you need an array instead?
- How did you record raffle entries so that a player who enters three times has
  three times the chance of winning?
- How did you count unique players separately from total entries?

I would use a struct combined with mapping to allow for easier access of the the raffle details, and an Array to store the different raffles(structs).
The use of structs allows details like the raffle owner and id to be bundled together, thus providing for multiple entries per user.

---

### 2. Security Measures

- **Reentrancy:** show the order of operations in `approveAndPay`. Which line
  updates the status, and which line sends the ETH? Why that order?
- **Access control:** which functions are owner-only or employer-only, and what
  would go wrong without those checks?
- **Input validation:** what did you reject, and where?

[Write your response here]

---

### 3. Randomness - Be Honest Here (4 marks)

You were allowed to use block data for the raffle draw. This section is where
you show you understand what that costs.

- What exactly does your randomness depend on?
- **Who can manipulate it, and how?** Name the actor and the action.
- What would you use in production instead, and why is that better?

[Write your response here]

---

### 4. Trade-offs & Future Improvements

- What did you not finish, or knowingly do the quick way?
- What would you add with another day? (dispute resolution, refunds, prize
  tiers, gas optimisation)

[Write your response here]

---

## REAL-WORLD DEPLOYMENT CONCERNS

> [!NOTE]
> These are **written questions only**. You are not deploying anything, and you
> do not need a wallet, a faucet or any test ETH to answer them. Reason it
> through in prose.

### 1. Gas Costs

- Which of your functions is the most expensive, and why?
- Roughly what would it cost a user at 20 gwei, with ETH at $3,000? (Use the
  same arithmetic as Part A Question 2.)
- Is that affordable for the users you would actually be building this for? If
  not, what would you change?

[Write your response here]

---

### 2. Scalability

**What happens when the raffle has 10,000 entries?**

- Which part of `selectWinner` gets slower or more expensive as the array grows?
- What breaks first?

[Write your response here]

---

### 3. User Experience

**How would you make this usable for someone who has never held a wallet?**

- What is the hardest step for a first-time user?
- If you *were* deploying this for real, which testnet would you try it on
  first, and how would a tester get test ETH? (Describe it - you are not doing
  it.)

The hardest step for a first-time user is interacting with the network. If i were to deploy this, i would deploy it on Sepolia. A tester would need a Faucet wallet, and to get test ETH there are a number of ways but the easiest way i know how is to download Metamask and create a wallet then activate the Sepolia testnet. The next step would be to fund the wallet using the likes of the Google Sepolia Faucet service.

---

## MY LEARNING APPROACH

### Resources I Used

Be specific. "The Cyfrin course" is not a resource; "Blockchain Basics, The
Oracle Problem" is. List 3-5.

Blockchain Basics course on Cyfrin Updraft
Solidity Smart Contract Developer course on Cyfrin Updraft
Google Gemini Guided learning Application

---

### Challenges Faced

- The biggest thing you got stuck on
- How you got unstuck
- What you know now that you did not this morning

The biggest thing i got stuck on was the code implementation section of this assessment, the level is way more advanced than i anticipated and the reality is without 
prior learning there is no way for me to get unstuck unless i retreat and continue cultivating. in short, i didn't get unstuck. I now know the importance of advanced
Solidity concepts in writing robust smart contracts.

---

### What I'd Learn Next

My future learning goals are to expand my knowledge on advanced Solidity concepts to position me as a better Solidity Smart Contract Developer by finishing the courses
i enrolled to on Cyfrin Updraft. To be specific to complete all 3 Solidity smart contract developer courses.

---
