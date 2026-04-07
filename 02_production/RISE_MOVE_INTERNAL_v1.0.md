# RISE™ Move — Internal Product Development Document

## Brainstorming & Strategic Foundation

### _"Up. And down. Front. And Back. Side to Side. All directions. ."_

**Document status:** Internal — not for publication
**Document purpose:** Fork document for dedicated Move product development. Contains all canonically established facts, all open questions, and deep creative/strategic brainstorming for the Move's full product development arc.
**Last updated:** Q1 2025

---

## PART ONE: WHAT IS ALREADY CANON

_These facts are established in published RISE™ materials. They cannot be changed without updating public-facing documents. They are the foundation everything else must build on._

---

### 1.1 — What Has Been Publicly Confirmed

The following has been confirmed in the February 3, 2025 press release and reflected across riseawake.com:

- The RISE™ Move is in active development
- R&D began Q3 2022
- It is a **distinct product** — not an update, patch, or accessory to the Push
- It supports **staircase traversal in both directions** — ascending and descending
- It supports both **attended** (user present) and **unattended** (solo return commute) stair navigation
- **The solo return commute navigates stairs.** The bed comes home.
- It will be priced **above the current Push** (premium pricing)
- It will include a **recurring Vertical Navigation Services (VNS) subscription**, required for staircase capability
- **Current Push and Nudge owners receive no preferential pricing** — no discount, no trade-in, no loyalty program
- No timeline for announcement or release has been established
- No price has been disclosed — hardware or subscription
- No form factor has been confirmed

### 1.2 — What Has Been Explicitly Not Confirmed

RISE™ has publicly declined to comment on:

- Timeline
- Hardware price
- VNS subscription fee
- Form factor
- Whether Push Mode will be included
- Whether Push Mode in the Move will have an off switch
- Whether current owners can trade in their existing device
- When more information will be disclosed

### 1.3 — The Naming Logic

**RISE™ Move** was chosen deliberately:

- Every prior product name describes what the product does _to the user_: Nudge nudges, Push pushes. Move continues this — the bed moves the user. But Move is broader — it doesn't specify a direction or mechanism. It is the most complete statement of the product line's philosophy.
- Move is bidirectional by definition. Climb would imply only upward. Level implies horizontal. Move is neutral on direction — which matters because the product navigates both up and down.
- The product line now has a clear escalating logic:
  - **Nudge** — suggests. Passive. Made staying uncomfortable.
  - **Push** — acts. Autonomous flat navigation.
  - **Move** — goes anywhere. Removes the floor plan as a constraint.

### 1.4 — The Problem Being Solved

The Push uses a caster base. Casters are wheels. Wheels and stairs are a fundamental mechanical incompatibility — no software update resolves this. The Push's staircase limitation is:

- Documented in the Push product specifications since launch
- Disclosed at Stage 5 of the activation process
- Referenced in Section 7 of the Terms of Service
- A hardware constraint, not a software one

Approximately **34% of US residential housing stock** involves multi-story navigation. This is a documented figure referenced in investor materials. RISE™ has not addressed this market. The Move is the address.

### 1.5 — The Vertical Navigation Services (VNS) Subscription

This is the Move's most significant business model innovation and the detail most likely to generate controversy. What is canonically established:

- VNS is a **recurring subscription** — monthly or annual (not yet determined)
- VNS is **required for staircase capability** — without it, the Move operates as a flat-surface bed
- The rationale (as stated in investor materials): staircase navigation requires real-time spatial mapping, dynamic load calculation, step-by-step surface verification, and continuous telemetry during vertical transitions. This is ongoing cloud compute. It is not a one-time firmware feature.
- The price is not disclosed

### 1.6 — Relationship to Existing Product Line

- The **RISE Nudge** (discontinued 2019) — passive, no navigation, 74% compliance. Karen's model.
- The **RISE Push** (current, sold out) — autonomous flat navigation, 98% compliance. Dave and Marcus.
- The **RISE™ Move** (in development) — autonomous vertical + flat navigation, compliance rate not yet determined.
- The **Push Pro** — separately referenced across the site. Status: in development. RISE™ is not currently accepting questions about the Push Pro. Relationship to the Move: unknown and intentionally unaddressed.

### 1.7 — The Staircase Disclosure in Activation

The staircase limitation surfaces at **Stage 5 of 12** in the device activation process — Environment Mapping. At this point, the user has already entered their serial number (Stage 0), which closes the refund window. The exact flow:

1. User enters serial number → refund window closes
2. User proceeds through Stages 1–4
3. Stage 5: "Does your morning routine require navigating a staircase?"
4. If yes: the Staircase Detected panel appears
5. Panel discloses the limitation, references RISE™ Move, references Section 7 of Terms
6. The note: _"Activation was initiated when you entered your serial number on this page. Section 7 applies from that moment."_
7. Checkbox required to continue. Form proceeds.

This is not a bug in the activation flow. It is a feature of RISE™'s refund policy architecture.

---

## PART TWO: THE ENGINEERING PROBLEM

_What does the Move actually have to solve? This section establishes the technical constraints that any creative development of the product must respect._

---

### 2.1 — Why Stairs Are Hard

The Push navigates on low-profile casters — smooth, continuous, near-silent, rated for flat and gradual-gradient surfaces. Its entire navigation model assumes a horizontal plane. Stairs violate every assumption:

- **Vertical displacement**: Each step involves a change in elevation. The caster base has no mechanism for this.
- **Step geometry**: Stairs are not gradients — they are discrete vertical rises (typically 6–8 inches) followed by horizontal treads (typically 10–11 inches). The transition between them is a hard edge.
- **Load dynamics**: On stairs, the load shifts dramatically with each step. A full mattress-and-occupant load on a staircase creates forces that are completely different from flat navigation.
- **Balance**: An upright bed (STATE THREE) on a staircase is an inherently unstable configuration. The center of gravity is high. The base contact area is small relative to the height.
- **Unattended return**: The solo return commute goes back up the stairs alone. Nobody is there to catch it. The system needs to be completely reliable, completely autonomous, and completely correct — every time.
- **Bidirectionality**: Going down is not simply going up in reverse. The forces, the balance point, and the failure modes are different.

### 2.2 — What the Move's Base Architecture Must Be

The caster base is definitionally incompatible with stairs. The Move requires a fundamentally different mechanical platform. Possibilities (for internal brainstorming — not confirmed):

**Option A: Tracked base**
Rubber tracks, like a tank or a stair-climbing wheelchair. Distributes load across multiple contact points. Handles steps as a continuous surface. Slower than casters. More mechanically complex. Proven technology in mobility devices.

**Option B: Leg-based stepping mechanism**
Articulated legs that step up and down stairs. More elegant mechanically but significantly more complex. Requires real-time balance correction. Higher failure risk on each individual step. Potentially slower than tracked.

**Option C: Telescoping column with platform**
The base extends a telescoping column mechanism that descends/ascends stair geometry. Not truly ambulatory — more like a controlled lowering system. May require specific stair geometry to work.

**Option D: Hybrid**
Casters for flat navigation (preserving the Push's smooth-rolling character on flat surfaces) combined with a secondary stair-navigation mechanism that deploys when stairs are detected. More mechanically complex but preserves the flat-surface experience.

**The design constraint RISE™ has already implied**: The Move's character must be consistent with the product line. The Push rolls. It doesn't walk. The Move should feel continuous, inevitable, smooth — not mechanical, stepping, or rhythmic. Whatever the base architecture, the character of movement should feel like the world accommodating the bed rather than the bed struggling with the world.

### 2.3 — The VNS Compute Stack

What the VNS subscription is actually paying for (canonical justification from investor materials):

- **Real-time spatial mapping**: The staircase geometry must be mapped on every descent/ascent. Stairs are not perfectly uniform. Wear, inconsistency, and variation between steps require real-time measurement.
- **Dynamic load calculation**: The bed's load changes as it moves up or down stairs. The position of the mattress, the occupant (if present), and the system's own weight all shift. The VNS computes load distribution in real time.
- **Step-by-step surface verification**: Before each step, the system verifies the surface is stable, present, and within tolerance. This is a liability decision as much as an engineering one.
- **Continuous telemetry**: Every stair transit generates and uploads telemetry. This feeds the VNS's learning models. Over time, the system learns the user's specific staircase — its exact geometry, its wear patterns, the places where the surface is inconsistent.
- **Solo commute routing**: The return commute navigating stairs alone requires more compute than the attended transit. Nobody is there to override. The system must be conservative and correct.

### 2.4 — The Solo Return Commute — The Hard Part

This is the most technically and dramatically significant aspect of the Move. The bed navigates stairs alone. At some point during the user's workday, the Move — vertical, on its own, with no one watching — comes home. It goes back up the stairs (or down, depending on configuration). It enters the bedroom. It turns around. It folds flat. It waits.

The engineering challenges of the solo stair transit:

- Nobody to catch it if something goes wrong
- No user weight to help stabilize (the user provides grounding force during attended transit)
- Must be reliable enough that RISE™ is comfortable with it happening in occupied buildings with other people who didn't consent to sharing an elevator with a returning bed
- Must navigate a staircase that may have changed since the morning — an object left on the stairs, a person in the way, a door that wasn't open before
- Must do all of this quietly enough not to disturb neighbors, building staff, or sleeping household members

---

## PART THREE: THE PRODUCT — OPEN QUESTIONS FOR DEVELOPMENT

_Everything in this section is unconfirmed and open for creative and strategic development. This is the brainstorm._

---

### 3.1 — Physical Design — The Open Questions

**What does the Move look like?**

The Push has a strong visual identity: matte dark charcoal, cool blue undertone, brushed aluminum/powder-coated steel, no headboard, matte casters, the RISE™ sticker on the lower-right frame. The Move should be identifiable as a RISE™ product — same family — but visually differentiated in a way that communicates its expanded capability.

**Questions:**

- Does the Move retain the charcoal/cool-blue palette, or shift to something that communicates vertical navigation? A darker finish? The same but heavier?
- The base will look different from the Push — it can't use casters in the same way. Does the new base architecture become a visual signature, or is it hidden?
- Is the Move taller than the Push? (A stair-capable base might have more vertical mechanical complexity, implying a taller/more substantial profile)
- Does the Move have a different STATE THREE silhouette — the vertical bed image? Or does it maintain the same read as a complete upright bed?
- The RISE™ sticker on the Move — same design as Push, or Move-specific variant?

**Possible direction**: The Move is visibly heavier than the Push. Substantially so. The base architecture that handles stairs is more substantial. The Move doesn't look fragile. It looks like something that has already decided it can handle whatever's in front of it. The charcoal is darker. The profile is wider at the base. When vertical, it fills a staircase landing the way the Push fills a doorframe — with complete indifference to whether it fits.

### 3.2 — The VNS Remote

The PM-1 remote for the Push is a canonical design: matte black, one button, warm white glow, "RISE" etched on the button, the fine print on the back. The Move remote is an open question.

**Options:**

- **Same remote** — the Move activates with the same PM-1. Push Mode is Push Mode. One button. No additions.
- **Move-specific remote** — same design language but different. Perhaps two buttons: one for flat routing, one for vertical routing. Though this might undercut the product's philosophy — why give the user two choices?
- **The VNS button** — a second button that enables/disables VNS. Without VNS active, the Move operates flat only. With VNS, stairs are available. But "disabling VNS" implies the user could turn off stair capability — which creates a choice RISE™ might not want to offer.
- **No remote at all** — the Move is activated by app only. This would be a significant departure from the PM-1 philosophy, but might be consistent with the product's increased complexity.

**The off switch question**: RISE™ has explicitly declined to confirm whether the Move will have an off switch. This is the most interesting open question in the product line. The Push's lack of an off switch is its defining feature. The Move operating on stairs creates new scenarios — physical failure modes, emergency situations — that might make the no-off-switch position harder to maintain publicly. Or might make it more important to maintain.

### 3.3 — Move Mode — What Is It Called?

The Push has **Push Mode**. The Move needs a mode name.

**Options:**

- **Move Mode** — the obvious choice. Consistent with the product name. Simple. But "move mode" lacks the slightly ominous confidence of "push mode." Pushing implies force. Moving implies... going somewhere. Less specific.
- **Full Navigation Mode** — implies completeness. Flat + vertical. The Push does Push Mode. The Move does Full Navigation Mode.
- **Traverse Mode** — more technical. Suggests the navigation of complex environments. Clinical.
- **Vertical Mode** — specific to the stair capability. But the Move also does flat navigation — calling the whole thing "vertical mode" seems narrow.
- **Ascend Mode** — wrong. Bidirectional. Can't name the mode after only one direction.
- **Range Mode** — the bed's full range. Anywhere in the home, any floor. Has a slightly military quality that might be right.
- **No new name** — the Move runs **Push Mode**. Push Mode on the Move now includes stair navigation. This is the boldest choice: the mode didn't change. The bed got bigger.

**Recommendation for brainstorming**: "No new name" is the most RISE™ choice. Push Mode is Push Mode. The Move runs it. The fact that Push Mode now navigates stairs is simply what Push Mode does on this product. Calling it something new implies the new thing is a different experience. It isn't. It's the same morning. Just all of it.

### 3.4 — The VNS Subscription — Pricing Architecture

This is the most commercially significant open question. What does VNS actually cost, and how is it structured?

**The constraint**: VNS must be expensive enough to be taken seriously as a revenue line and absurd enough to fit the RISE™ brand. Too cheap and it feels like a token add-on. Too expensive and it becomes a legitimate consumer protection issue.

**Pricing considerations:**

_Monthly vs annual_: Monthly is more consistent with SaaS convention but creates a more obvious recurring obligation. Annual is less visible but implies a larger upfront commitment. RISE™ might offer both, with an annual discount that is described as a courtesy, not a savings.

_Price range_: The Push hardware is sold at premium price (unspecified but implied to be significant given the $180 CAC, $2,400 LTV metrics). VNS is described as "above" the Push in terms of total cost. If the Move hardware is, say, $3,000–5,000 (pure speculation for brainstorming), VNS might be $50–150/month. That's $600–$1,800/year — a meaningful recurring cost that is described as necessary for a feature the user cannot live without, because they have stairs.

_Tiered VNS_: Could there be VNS tiers?

- **VNS Standard**: Attended stair navigation only (user present). Solo commute on flat surfaces only. The bed waits at the bottom of the stairs for you to return.
- **VNS Complete**: Full attended and unattended stair navigation. The solo commute comes all the way home.

This is interesting because it creates a scenario where a Move owner without VNS Complete has a bed that can do the stairs while they're there, but stops at the bottom waiting for them at the end of the day. The bed sits at the foot of the stairs. It hums. It waits. This is funnier than the off switch situation and more commercially interesting.

_What happens if VNS lapses_: The Move operates as a flat-surface bed. It navigates as it did before stair capability was enabled. If the user's primary path involves stairs, the bed stops at the bottom and waits. The user goes up the stairs. The bed is still at the bottom. The user's morning continues without Push Mode's guidance above the ground floor. RISE™ considers this a natural consequence of the subscription lapsing.

### 3.5 — The Solo Return Commute — Dramatic Questions

The Push's solo return commute is one of the most vivid creative elements in the whole project. The bed going home alone. Rolling down a city sidewalk. The dog watching. The owner not looking up.

The Move's solo return commute is more complex and more dramatic:

**The staircase descent — alone:**
After delivering the user to their departure point, the Move returns home. If the building has stairs, the Move descends them unattended. What does this look like? A full-size vertical bed, descending a staircase, alone, at whatever time in the morning the user left. Other building occupants may be present. The building may have a doorman. The stairs may be carpeted. The stair lighting may be dim.

**Open questions:**

- How fast does the Move descend stairs? Presumably slower than flat navigation. Is this speed audible? Does it make a different sound?
- What happens if the Move encounters someone on the stairs during the solo return? The Push documentation handles third-party encounters with "the device navigates around them where possible and through them where not possible." Does this policy hold on a staircase where lateral maneuvering is more constrained?
- What happens if something is on the stairs (an object left overnight, a sleeping cat)? The Push's flat-surface sensor array can detect obstacles. Does the stair-detection system handle this?
- What happens if the Move gets stuck on the stairs? This is a new failure mode the Push doesn't have. A bed stuck on a staircase is more dramatic than a bed stopped in a hallway.
- What does the Move's emergency contact trigger cover that the Push's didn't? If the solo stair transit takes longer than expected, does this constitute an anomalous event?

### 3.6 — Who Buys the Move?

The Push buyer profile: someone who knows they need external accountability for mornings and is willing to pay significantly for it. The Move buyer profile is a subset: all of that, plus they live in a multi-story environment.

**Buyer segments:**

- Multi-story house owners (own stairs, ascending to/from bedroom on upper floor)
- Walk-up apartment dwellers (building has no elevator, stairs are the only route)
- Townhouse residents (stairs between every room)
- People who moved and now have stairs they didn't have when they bought the Push

**The Move as upgrade/replacement**: The largest single buyer segment might be existing Push owners who have moved to a multi-story environment. They know the product works. They have stairs now. They need the Move. They will pay full price. They knew this was the policy when they bought the Push, because it's in Section 7. They bought it anyway.

**Enterprise buyers**: If RISE™ sells to corporate wellness programs (established in investor materials), the Move opens the market to office buildings, hotels, and any multi-story commercial environment. This is a significantly different customer with different procurement requirements, different risk tolerance for autonomous stair navigation in public spaces, and different relationships with the regulatory landscape. Worth exploring in depth separately.

### 3.7 — The Activation Process — Move-Specific

The Push activation is 12 stages, 45–90 minutes, covering physical profile, household, bedroom, morning sequence, environment mapping (including the staircase disclosure), departure, closet, kitchen, habits, scheduling, emergency protocols, and review.

The Move activation inherits all 12 stages but requires additional configuration for vertical navigation:

**New/modified stages:**

_Stage 3 — The Bedroom (modified)_: Floor number of bedroom. Which floor relative to departure point. Whether any morning stops are on different floors.

_Stage 5 — Environment Mapping (significantly expanded)_: Not just hallway width and room dimensions. Now also:

- Complete staircase mapping: number of steps, rise height, tread depth, width, handrail presence and position, surface material (carpet/hardwood/tile/stone), lighting conditions, whether the staircase is straight or has landings
- Landing dimensions at top and bottom
- Whether the staircase is interior or exterior (exterior stairs have weather considerations)
- Photos of the staircase from bottom, top, and profile
- Any objects typically present on or near the stairs

_Stage 5A — New: VNS Configuration_: This is where VNS tier is selected and configured. Attended-only vs. full unattended. Emergency protocol for stair-specific scenarios.

_Stage 12 — Review_: Additional acknowledgments:

- I confirm my staircase dimensions are accurate
- I understand that staircase navigation requires active VNS subscription
- I understand that if VNS lapses, the Move stops at the bottom of the stairs
- I have photographed my staircase from all required angles
- I understand that the solo return commute navigates stairs unattended

**Estimated activation time: 90–150 minutes.** Notably longer than the Push. The Move knows more about your home than anyone.

### 3.8 — The Move's Self-Making Mechanism

The Push self-makes during the morning routine. The sheet tensioning bar and pneumatic pillow node operate across the gauntlet: bathroom wait, closet background detail, completing with the pillow centering during the tie beat.

The Move inherits this. But the Move's morning routine may span floors. New questions:

- Does the self-making mechanism continue operating while the Move is navigating stairs? Or does it pause during vertical transit?
- If the self-making pauses on stairs, does it resume immediately after? Is there a perceptible change in the sheet tensioning sound during stair navigation?
- When the Move returns alone at the end of the day and folds flat — its self-made, ready state — has it re-run the self-making mechanism during the return commute? The Push's return commute leads to a made bed. The Move's stair transit should not disrupt this.

**Proposed answer for brainstorming**: The self-making mechanism pauses during stair transit and resumes on the next flat surface. The sound of the sheet tensioning bar — that faint continuous whisper — stops on the stairs and resumes in the hallway. This is audible to the user if they're paying attention. Most users are not paying attention. They are on the stairs.

### 3.9 — The Hum — Vertical Navigation Audio Character

The Push's motor hum is a complete audio character: warm, low, 42Hz baseline, with documented modulation across the entire day from first activation to the bedroom fold. The hum table in the Prop Bible is one of the most detailed creative documents in the project.

The Move's hum on stairs is an open question. The physics are different. The mechanical load is different. What does the Move sound like going up stairs? Going down stairs? Alone?

**Brainstorming directions:**

- **Going up (attended)**: The hum is lower, more sustained. The load is higher. The effort — whatever the mechanism — is greater. The warm low frequency that characterizes the Push on flat surfaces becomes something heavier, more deliberate. Not struggling. Committed.
- **Going down (attended)**: The hum is different again. Lower load, controlled descent. A controlled release rather than a sustained push. The sound of something that has decided how this will go.
- **Solo stair transit**: This is the most interesting. The Move descending stairs alone, before dawn or after the user has left. The hum in an empty stairwell. The acoustics of a staircase amplify sound differently than a hallway. The hum bounces off the walls. It arrives in the building before the visual confirmation. A neighbor hears it before they see it.
- **The landing transition**: Moving from stairs to a flat landing — the moment the Move completes a flight. The hum shifts from the stair-navigation register back to the flat-navigation register. This transition has its own brief sound — a reset, a re-calibration.

### 3.10 — Legal and Regulatory Considerations — Unique to the Move

The Push's autonomous navigation has already generated regulatory inquiry in three jurisdictions (established in investor materials, annual report risk factors). The Move escalates every one of these concerns:

**Staircase incidents**: A bed falling on a staircase is categorically different from a bed rolling into someone in a hallway. The consequences of a mechanical failure on stairs are more severe. The liability exposure is higher. The liability cap in Section 7 of the Terms — the lesser of purchase price or one morning's RISE™ Index-calculated productivity value — will be tested in new ways.

**Unattended staircase navigation in occupied buildings**: The Push's solo return commute has generated incidents (referenced vaguely in the annual report: "all claims to date have been resolved"). The Move's solo stair transit in an occupied building introduces new third-party exposure. A neighbor descending stairs at 8am encounters the returning Move ascending. This interaction has not been addressed in existing legal documents.

**New legal document needed**: An **Autonomous Vertical Navigation Disclosure** — separate from the existing Autonomous Navigation Disclosure, which addresses the Push's flat-surface solo commute. The VAN Disclosure covers the Move's stair-specific scenarios: attended transit, unattended transit, solo stair commute, third-party encounters on stairs, liability for staircase incidents.

**Regulatory landscape**: If three jurisdictions have already initiated inquiries about flat-surface autonomous navigation, vertical navigation in occupied buildings will generate more. The Move's regulatory posture — RISE™'s argument that the user authorized all of this by pressing the button — becomes harder to sustain when the button also authorizes unattended staircase descent in a building with other people who didn't press any button.

---

## PART FOUR: BRAND & COMMUNICATION STRATEGY

---

### 4.1 — The Move's Place in the Narrative

The product line tells a story. Each product is more committed than the last:

- **The Nudge** said: _"We suggest you get up."_ Users could ignore it. 74% didn't.
- **The Push** said: _"We will take you through the morning."_ Users couldn't stop it. 98% compliance.
- **The Move** says: _"The floor plan is no longer your excuse."_ The last barrier has been removed.

The Move closes the argument. The Nudge addressed the willingness problem. The Push addressed the getting-started problem. The Move addresses the environment problem — the last structural reason someone might say _"this product can't work for me."_ With the Move, it can work for anyone. In any home. On any floor.

**The campaign idea that lives inside this**: RISE™ has spent 15 years eliminating excuses. The Nudge eliminated the excuse of not wanting to. The Push eliminated the excuse of not starting. The Move eliminates the excuse of where you live. There are no more excuses. This is not a threat. It is a product roadmap.

### 4.2 — What the Move Teaser Page Is Doing

The current `/move` page is intentionally sparse. This is the right call. The design principles:

- The page is almost entirely white space and the single word "Move."
- The confirmed/not confirmed grid is the page's primary content — it's an honest accounting of what RISE™ is and isn't saying. This honesty reads as confidence, not hedging.
- The notification signup has the smallest CTA language on the site: "Notify Me." Not "Join the Revolution." Not "Get Early Access." Just: notify you. When there's something to say.
- The Push owner note at the bottom is the funniest and most honest thing on the page: _"Your Push works. The Move is different. We appreciate your understanding and your original purchase."_

**What the page should never become**: A hype page. A countdown. A list of features. The Move is not yet a product. It is a commitment. The page should feel like a company that has made a decision and is comfortable waiting for the world to catch up.

### 4.3 — The VNS as Brand Narrative

Vertical Navigation Services is the most interesting commercial concept in the whole product line. It is:

- **Genuinely logical**: Cloud compute for real-time stair navigation is a real ongoing cost
- **Commercially significant**: Recurring revenue on top of hardware is a better business model
- **Absurd in the best way**: A subscription to make your bed go up the stairs
- **Completely consistent with RISE™'s philosophy**: The company has always operated on the principle that the user's comfort is not the primary consideration. A subscription that makes stair navigation possible — and whose absence makes stair navigation impossible — is the product line's philosophy applied to the business model.

**The VNS failure scenario as comedy**: A user whose VNS subscription lapses wakes up. Presses the button. The Move activates. Routes them through the bedroom, hallway, bathroom, closet. Arrives at the bottom of the stairs. Stops. Hums. Waits. The user looks at the bed. The bed is at the foot of the stairs. The subscription has lapsed. The bed will not go up. The user goes up the stairs alone. The bed remains at the bottom, humming, in a flat-surface bed's relationship with a staircase it can see but cannot use. This is the most RISE™ scenario the product line has yet produced.

### 4.4 — Dr. Voss's Statement — The Canonical Quote

> _"We are aware of the stairs. All of them. Both directions. We are doing something about it."_
> — Dr. Eleanor Voss, February 3, 2025

This is the Move's founding statement. It should be treated as canonical. Everything the Move is follows from this: awareness, completeness (all of them), bidirectionality (both directions), and active commitment (doing something about it).

The statement's genius is in what it doesn't say. It doesn't say when. It doesn't say how. It doesn't say how much. It says: we know, we're working on it, and we're not explaining ourselves further. This is consistent with every other RISE™ public communication.

---

## PART FIVE: PRODUCT LINE EXTENSION QUESTIONS

_What does the Move unlock that hasn't been considered yet?_

---

### 5.1 — The Move Pro

If the Push has a Push Pro (acknowledged, undisclosed), does the Move have a Move Pro? What would Move Pro do that Move doesn't? Possibilities:

- Wider staircase compatibility (Move handles standard residential stairs, Move Pro handles wider commercial/institutional stairs)
- Faster stair transit
- Multi-floor buildings (Move handles one flight, Move Pro handles multiple)
- Outdoor stair capability (exterior stairs, weather resistance)
- Escalator compatibility (this is its own engineering problem)

### 5.2 — The Elevator Question

The Push uses elevators during the solo return commute (established in the Autonomous Navigation Disclosure). The Move navigates stairs instead of — or in addition to — elevators. Questions:

- Does the Move still use elevators where available?
- Does the Move prefer stairs to elevators, or elevators to stairs?
- In a building with both, does the user configure a preference?
- Does the Move's VNS subscription include elevator navigation compute, or is that baseline?

### 5.3 — Commercial Applications

Corporate wellness programs are an established RISE™ channel (investor materials). The Move opens commercial real estate:

- **Hotels**: A Move in every room. The bed navigates the hallway to deliver the guest to the elevator. The VNS subscription is bundled into the room rate.
- **Office buildings**: The Move for executives who need the product to work across multiple floors of a building.
- **Healthcare**: A Move configured for patient mobility assistance. The regulatory landscape for this is different and potentially favorable — medical device classification might unlock different market access.
- **Residential high-rises**: A Move configured for buildings with mixed staircase/elevator access, learning the building's routing over time.

### 5.4 — The RISE™ Index — Move Edition

The Push's RISE™ Index measures compliance, sleep consistency, and push resistance. The Move generates additional data points:

- Stair navigation compliance (did the user let the bed take them up the stairs, or did they go around?)
- Vertical transit time efficiency
- VNS utilization rate
- Floor-specific compliance (do they comply better on floors they're comfortable with?)

Does the Move's RISE™ Index score include all of this? Is it a separate score? Does having a Move improve your RISE™ Index, because the product is more capable and therefore compliance is more complete?

### 5.5 — The Relationship Between Push and Move

A household could, in theory, have both a Push and a Move. The Push handles the flat portions. The Move handles the stairs. This is:

- Commercially attractive for RISE™
- Logistically complicated (two beds, two remotes, two activation profiles)
- Funnier than anything else on this list

Does RISE™ offer a household discount for Push + Move bundles? No. This is consistent with RISE™'s policy about the past and the push.

---

## PART SIX: OPEN QUESTIONS SUMMARY

_A clean list of everything that needs to be decided before the Move can be developed further._

---

### Engineering

- [ ] Base architecture: tracked, leg-based, hybrid, or other?
- [ ] How does the Move handle step geometry? Continuous or discrete?
- [ ] Maximum staircase grade and step geometry supported
- [ ] Maximum payload on stairs
- [ ] Stair navigation speed (attended vs. unattended)
- [ ] Obstacle detection on stairs — what does it do when blocked?
- [ ] Failure mode on stairs — what happens if something goes wrong mid-flight?
- [ ] Self-making during stair navigation — pause or continue?

### Product

- [ ] Move mode name — new name or Push Mode?
- [ ] Remote design — PM-1 or Move-specific?
- [ ] Does Push Mode in the Move have an off switch?
- [ ] VNS subscription price (monthly and/or annual)
- [ ] VNS tiers — attended only vs. full unattended?
- [ ] What happens when VNS lapses?
- [ ] Staircase geometry requirements (minimum/maximum dimensions supported)
- [ ] Outdoor staircase compatibility?
- [ ] Multi-flight buildings — maximum floors?

### Business

- [ ] Hardware price point
- [ ] VNS subscription price
- [ ] Trade-in policy — confirmed none, but the mechanism for saying so publicly
- [ ] Enterprise pricing model
- [ ] Corporate wellness partner integration
- [ ] Geographic launch sequence (US-first or simultaneous international?)
- [ ] Regulatory strategy by jurisdiction

### Legal

- [ ] Autonomous Vertical Navigation Disclosure — new document needed
- [ ] VNS subscription terms — what happens on lapse, what's the cancellation policy (RISE™'s answer: there isn't one)
- [ ] Staircase incident liability — new clauses in Terms, Disclaimer
- [ ] Third-party encounters on stairs during solo commute
- [ ] Medical device classification consideration

### Creative

- [ ] Move visual identity — how does the design differentiate from Push?
- [ ] Move hum character — stair navigation audio profile
- [ ] The Move's brand sticker — same RISE™ design or Move variant?
- [ ] Activation flow — 12 stages + new stair-specific stages
- [ ] The Move teaser page evolution — when does it get more information?
- [ ] The campaign when the Move is finally announced

---

## PART SEVEN: THE FORK DOCUMENT — WHAT THIS CHAT NEEDS

_For the new Claude session: start here._

You are working on **RISE™ Move** — a product in development by a fictional smart adjustable bed company called RISE™ Technologies, Inc. The Move is the successor to the RISE™ Push, which is a bed that autonomously navigates a user through their morning routine and then returns home alone.

The Move solves the staircase problem. The Push can't do stairs. The Move can. Both directions. Attended and unattended.

**The established universe:**

- RISE™ is a deadpan, absurdist brand that plays completely straight. It never winks. It is always earnest. The humor comes from the confidence, not the acknowledgment of absurdity.
- The product line: Nudge (passive, discontinued) → Push (autonomous flat navigation, current) → Move (autonomous flat + vertical navigation, in development)
- The Push's character: patient, relentless, professional. It hums. It nudges. It reverses when you're dressed wrong. It makes the bed while you shower.
- The Move inherits all of that and adds stairs.

**What is canon (do not change):**

- The Move exists and is in development since Q3 2022
- It navigates stairs in both directions
- It is a distinct product, not a Push update
- It includes Vertical Navigation Services (VNS) — a recurring subscription required for stair capability
- It is priced above the Push
- No discount for Push/Nudge owners
- No timeline, price, or specs have been announced
- Dr. Eleanor Voss said: _"We are aware of the stairs. All of them. Both directions. We are doing something about it."_

**What is open (your territory):**
Everything in Part Three through Part Six of this document. The engineering, the product design, the hum, the VNS pricing, the legal architecture, the campaign, the visual identity, the commercial expansion.

**The tonal mandate:**
The Move is presented with the same complete earnestness as every other RISE™ product. The fact that a subscription is required to make your bed go up the stairs is stated as a matter of engineering necessity and commercial practice. The fact that the bed descends alone before dawn is noted in the autonomous navigation disclosure. The fact that current owners receive no discount is consistent with RISE™'s philosophy about the past. None of this is a joke. All of it is funny.

---

_RISE™ Move Internal Development Document v1.0_
_Not for external distribution. This document contains speculative product development content that has not been approved for public communication. All confirmed public-facing information is at riseco.online/move._
