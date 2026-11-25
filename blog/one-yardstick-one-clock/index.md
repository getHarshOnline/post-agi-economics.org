Title: One Yardstick, One Clock: why the AI timeline debate misses the point

[Read HTML](https://post-agi-economics.org/blog/one-yardstick-one-clock/)

Author: Harsh Joshi

<a id="one-yardstick-one-clock-why-the-ai-timeline-debate-misses-the-point"></a>

# One Yardstick, One Clock: why the AI timeline debate misses the point

“AI will take your job.”

Cool. But AI won't buy Nike, pay for Netflix or need a Tesla in the garage. If you replace workers faster than you create buyers, who exactly are you selling to?

Most takes stop there: doom or denial. I'm bored of both. It's time we put the pundits to a test. What I'm proposing is simpler: fix the yardstick and read the clock.

The yardstick judges execution against a measurable value function, a valid evaluator for that value and actual means to act: permissions, APIs and tools. Same inputs, same tools, same constraints. The clock asks how the surrounding economy changes, how long people have to adapt and which destination that change makes possible.

**Note**

**Time to Agent-Dominant Execution is research, with calculations to test and observations still to fit.** It has not produced an empirical forecast. A formula for a clock is a beginning; making it tell us something useful about the world is the work.

<a id="the-annoying-part-nobody-wants-to-hear"></a>

## The annoying part nobody wants to hear

My starting claim is that many apparent intelligence failures are failures to instrument the work. The value is vague, nobody can reliably judge the result, or the system has no means to act on its answer. A more capable model can still fail in that arrangement. The July 2025 Project NANDA report gave this problem a memorable headline about unsuccessful enterprise AI, but its findings about integration and learning do not establish a universal failure rate or prove my execution hypothesis.<sup><a id="fnref-note-6e616e6461"></a>[1](#fn-note-6e616e6461)</sup>

Take the invoice comparison used below. An assistant can produce a polished payment proposal while missing a discrepancy between the invoice and the authorised order. If the evaluator counts “proposal produced” as “case correctly resolved”, it rewards the appearance of completion. A warranted escalation and a correct proposal need to remain distinguishable from an unauthorised payment. Repairing that measurement makes the capability question answerable; it does not decide the question in the model's favour.

This is why I keep saying buy before you build for most teams. The tail from 90 to 99 percent is brutal: edge cases, pipelines, permissions, recovery and reliable operation. Those percentages describe the shape of the effort, not a measured success rate. You win by specifying the value, evaluator and means of action clearly, not by collecting model-zoo stickers. Ship the evaluators with the system.

<a id="one-yardstick-to-break-every-tired-argument"></a>

## One yardstick to break every tired argument

People argue past each other because they mix governance, what should we optimise, with execution, who can hit that target. Prices already help coordinate people who do not share all their information. Hayek's account of the price system makes that dispersed knowledge the problem to solve.<sup><a id="fnref-note-686179656b"></a>[2](#fn-note-686179656b)</sup> My extension is that a signal need not require a human recipient: a person or a machine can respond if it can interpret the signal and has the tools and permission to act.

That leaves the Agent Execution Hypothesis:

*If a workflow has a measurable value function, a valid evaluator for that value and actual actuators or permissions, an artificial agent can, in principle, match or exceed human execution under the same inputs, tools and constraints.*

This is a conjecture. Its prerequisites make the comparison possible; they do not prove the conclusion. A working test must name the agent class, human comparison, cases, resources and time available. If the evaluator cannot distinguish a useful result from a bad one, the attempt has not established an executable comparison. If the evaluator works and a candidate falls short, that is a result about the candidate tested. Neither outcome can be dismissed by quietly changing the task.

The hypothesis does not wave away tacit skill. If the know-how is in the wrists, its contribution has to become observable in the evaluation. Preferences or inverse reinforcement learning may help in a particular case, but they need validation too. If a valid evaluator cannot be built within the stated limits, the hypothesis does not apply to that attempt yet. Calling a skill unmeasurable and calling it absent are very different things.

[An invoice comparison](https://post-agi-economics.org/collections/thinking-gets-cheap/who-gets-the-gain/compare-complete-execution/) puts the distinction into ordinary work. Preparing a correct proposal and escalating an unresolved discrepancy can both be useful outcomes. Releasing money is another action with its own authority. The complete comparison counts review and correction, not just the speed of the first answer.

<a id="the-clock-with-its-assumptions-in-view"></a>

## The clock, with its assumptions in view

The clock models an economy moving among regimes. Capability, power, labour, credit and governance can change the probability of the next transition. Two proposed destinations distinguish agent-dominant execution with households able to buy from agent-dominant execution with weak household demand. Calling them absorbing states means the model cannot leave them once reached. Whether that is a defensible account of an economy is itself a research question.

Start with the simpler, fixed-transition calculation. Let $Q$ contain the probabilities of moving among the transient states. When its spectral radius is less than one, the fundamental matrix and expected steps to absorption are

$$
N=(I-Q)^{-1},\qquad \boldsymbol t=N\boldsymbol 1.
$$

For each initial transient state, the variance of the waiting time is

$$
\boldsymbol v=(2N-I)\boldsymbol t-\boldsymbol t\odot\boldsymbol t,
$$

where $\odot$ squares the entries individually. These are properties of the specified chain. They do not supply its probabilities or show that its states describe economic activity.

Changing probabilities require another calculation. With initial row distribution $\alpha$ and successive transient matrices $Q_0,Q_1,\ldots$, the probability of still waiting after $k$ periods is

$$
\Pr(T>k)=\alpha Q_0Q_1\cdots Q_{k-1}\boldsymbol 1.
$$

The order matters. Freezing today's transition matrix answers “what if today's rule persisted?”, not “what happens under tomorrow's changing conditions?”. [The time between frontiers](https://post-agi-economics.org/blog/one-clock-many-frontiers/) works through the difference with two clocks that have the same chance of crossing today and very different expected waits.

If the regimes are unobserved, a hidden-state model could estimate them from signals rather than assigning confident labels by hand. That introduces fitting, state-selection and identification questions before a forecast can be trusted.<sup><a id="fnref-note-68616d696c746f6e"></a>[3](#fn-note-68616d696c746f6e)</sup>

And a forecast has to meet its outcome. Issue it with the information available at a stated date, keep its original target and compare it with a credible baseline. Proper scoring rules such as Brier and logarithmic scores make confidence consequential. If the forecast underperforms, record the failure and revise under a new plan; don't rewrite the old forecast. [A forecast meets its outcome](https://post-agi-economics.org/collections/thinking-gets-cheap/models-and-measures/a-forecast-meets-its-outcome/) shows how that comparison works.

The pre-analysis plan belongs before that outcome: lock the signals, target, fitting choices, baselines and rules for revision so the answer cannot choose its own test afterwards. A Diebold–Mariano comparison can test the average loss difference between two forecast series under its assumptions, with dependence and sample size handled explicitly.<sup><a id="fnref-note-646d"></a>[4](#fn-note-646d)</sup> It is a comparison of forecasts, not an automatic verdict that one economic theory is true.

There is also a reflexivity problem. A published clock can change the investment, policy or behaviour it tries to forecast. The protocol therefore includes disclosure and update rules, an embargo on parameter changes, and monitoring of how the forecast is used.

<a id="but-innovation-but-reasoning-but-agi"></a>

## “But innovation\! But reasoning\! But AGI\!”

Machine novelty is possible without settling the question of sentience. AlphaGo's unfamiliar strategies gave human Go players something new to study.<sup><a id="fnref-note-616c706861676f"></a>[5](#fn-note-616c706861676f)</sup> Search can surprise us. Whether another system can make a useful novel contribution in another domain remains something to test, not a reason to exclude it by definition.

“AI needs prompts” also confuses an interface with a system. A programme can respond to a feed, webhook or market signal without somebody typing into a chat window. The useful question is what it can observe, how its response is judged and what it can actually do. A familiar textbox tells us little about that whole arrangement.

Automated research could accelerate the change. The possibility of AI systems helping build more capable AI is central to Aschenbrenner's *Situational Awareness* argument.<sup><a id="fnref-note-616363656c65726174696f6e"></a>[6](#fn-note-616363656c65726174696f6e)</sup> It belongs here as a possible influence on the transition, not a guaranteed timetable. A clock would need to measure the contribution rather than borrow the confidence of the story.

<a id="agents-still-don-t-buy-jeans"></a>

## Agents still don't buy jeans

An agent can perform a job without needing the wages with which its previous worker bought a service. That is why the clock keeps Buyer-Rich and Buyer-Thin outcomes separate. We need to ask what economy the agents are winning into.

The buyer question is not answered by counting jobs alone. Lower prices, new work, ownership income, public provision and transfers can change a household's resources. They have different recipients and different conditions. A cheaper service can help while an income loss elsewhere leaves its customer worse off. [Following household purchasing power](https://post-agi-economics.org/collections/thinking-gets-cheap/who-gets-the-gain/from-capability-to-economic-consequence/productivity-and-purchasing-power/) requires those channels to remain visible.

Governance decides the objective and the arrangements around the surplus. The clock asks how much time there may be to adapt them. It cannot establish a universal closing window by declaration. That needs a defined intervention, its lead time, a constraint that really becomes binding and evidence about when it does.

The fuller Post-AGI Economics inquiry develops alongside this clock. As cognition becomes cheaper, which other inputs become scarce? Who owns them? When does a familiar economic model still work, and when has it omitted the relation needed to understand the result? These questions refine the thesis without making its concern with time disappear.

<a id="if-you-build-build-like-this"></a>

## If you build, build like this

My engineering scars are why I keep coming back to evaluations as acceptance tests. Start with the value, the evaluator and the permitted actions. Check whether an existing capability can do the job before deciding to build one. Assume integration is the real boss level: the good answer still needs the right data, a dependable handoff and a way to recover when something fails.

The yardstick also needs a way to lose. Evaluator failure under the declared budget challenges whether the workflow can be instrumented. A named agent's shortfall challenges that execution claim. Persistent human–agent complementarity challenges a simple replacement story. An outcome that improves the metric while missing its purpose challenges the evaluator. Forecast underperformance challenges the clock. These are different failures, and they point to different work.

If you think the yardstick is wrong, propose a better value, evaluator and action specification. If you think the clock is wrong, compare its dated forecast with a better one when there is a forecast to test. Either way, we learn something more useful than another argument about a date.

For the capability question, [Beyond the Mirage](https://causality.in/blog/beyond-the-mirage/) (on Causality) proposes separate measures of causal understanding and agency. [Bubble or bridge?](https://rawthoughts.in/collections/ideas/india-ai/testing-indias-ai-crossing/bubble-or-bridge/) (on RawThoughts) takes the execution and complementarity questions into India's AI moment. [The Red Pill](https://post-agi-economics.org/blog/the-red-pill/) asks whether transferable intelligence could become a new unit of exchange; [Cheap copies, scarce attention](https://post-agi-economics.org/blog/cheap-copies-scarce-attention/) follows the constraints around easier production. These are connected questions; a good answer to one does not remove the need to test the others.

Pick a yardstick you can measure. Wire an evaluator you can trust. Give it actuators that actually do things. Then follow the result far enough to find out who gets paid, who gets to buy and how much time they have to adjust. The jeans still need a customer.

1. 
   
   <a id="fn-note-6e616e6461"></a>
   
   Challapally, Pease, Raskar and Chari, [*The GenAI Divide: State of AI in Business 2025*](https://static1.squarespace.com/static/6500af89e96bbc5786d1da01/t/6920be279a3693773f575e47/1763753511964/ai_report_2025.pdf), July 2025, preliminary findings from January–June 2025. The report combines a review of more than 300 public initiatives, interviews with 52 organisations and 153 conference survey responses. Its definitions and denominators vary; it notes that category sizes and organisational success definitions differ. This supports examining integration and contextual learning, not treating “95 percent” as a representative estimate of all AI projects or a controlled test separating instrumentation from model capability. [↩](#fnref-note-6e616e6461)

2. 
   
   <a id="fn-note-686179656b"></a>
   
   F. A. Hayek, [“The Use of Knowledge in Society”](https://oll.libertyfund.org/titles/hayek-the-use-of-knowledge-in-society-1945), *American Economic Review* 35(4), September 1945, pp. 519–530. The extension from people responding to price signals to artificial executors is the argument here, not a claim that Hayek established the Agent Execution Hypothesis. [↩](#fnref-note-686179656b)

3. 
   
   <a id="fn-note-68616d696c746f6e"></a>
   
   James D. Hamilton, [“A New Approach to the Economic Analysis of Nonstationary Time Series and the Business Cycle”](https://users.ssc.wisc.edu/~bhansen/718/Hamilton1989.pdf), *Econometrica* 57(2), March 1989. Hidden regimes are a modelling option; naming one supplies neither an observed regime nor a fitted transition clock. [↩](#fnref-note-68616d696c746f6e)

4. 
   
   <a id="fn-note-646d"></a>
   
   Diebold and Mariano, [Comparing Predictive Accuracy](https://www.nber.org/system/files/working_papers/t0169/t0169.pdf), 1994 working paper, published 1995; Diebold's [later account of the test's use and limits](https://economics.sas.upenn.edu/sites/default/files/filevault/12-035.pdf) distinguishes forecast comparison from model selection. [↩](#fnref-note-646d)

5. 
   
   <a id="fn-note-616c706861676f"></a>
   
   Demis Hassabis and David Silver, [“AlphaGo's next move”](https://deepmind.google/blog/alphagos-next-move/), 27 May 2017, describes the strategies and subsequent human experimentation. That example concerns Go, not general economic replacement. [↩](#fnref-note-616c706861676f)

6. 
   
   <a id="fn-note-616363656c65726174696f6e"></a>
   
   Leopold Aschenbrenner, [“From AGI to Superintelligence: the Intelligence Explosion”](https://situational-awareness.ai/from-agi-to-superintelligence/), June 2024. This is an acceleration thesis whose conditions and timing need examination, not an empirical result of One Yardstick. [↩](#fnref-note-616363656c65726174696f6e)
