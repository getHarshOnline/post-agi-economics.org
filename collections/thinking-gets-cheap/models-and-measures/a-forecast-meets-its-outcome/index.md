Title: A forecast meets its outcome

[Read HTML](https://post-agi-economics.org/collections/thinking-gets-cheap/models-and-measures/a-forecast-meets-its-outcome/)

Author: Harsh Joshi

<a id="a-forecast-meets-its-outcome"></a>

# A forecast meets its outcome

At the end of June, a model assigns probability 0.8 to an event in September: half of a stated group of firms will operate a particular invoice-preparation workflow at the required quality. September arrives. How should that forecast meet what happened?

The example is hypothetical, but it gives the timing problem something to answer to. A probability of 0.8 is neither a guarantee nor a way to remain right regardless of the result. It is a distribution whose confidence has consequences when scored. A useful [One Yardstick](https://post-agi-economics.org/one-yardstick/) clock would earn trust through such encounters: an event defined before its outcome, information available at the time, and a comparison with what a simpler forecast could say.

<a id="the-prediction-carries-a-date"></a>

## The prediction carries a date

The population, workflow and acceptance condition are part of the event; September and the June information cutoff are part of the prediction. Another forecast made in August can use August information. It answers the same target event from a different starting position and shorter horizon. An August model cannot be credited with a June prediction by fitting to the completed quarter afterwards. Similarly, a revised historical series may support a better present model while remaining unavailable to the original forecaster at the time. This is why a forecast needs an information vintage as well as a model version. When a forecast is issued, it can use only what could then be known. A later outcome can correct the observation; it cannot silently improve the earlier information set.

A forecast record separates what was known from what was later observed:

| Record | Origin and information cutoff | Target | Probability or outcome |
| --- | --- | --- | --- |
| First forecast | End of June | Stated September event | 0.8 |
| Updated forecast | End of August | The same September event | Its newly issued probability |
| Outcome | End of September | The original workflow, population and acceptance condition | Observed yes or no, or an explicitly missing observation |

The August update gets to learn from August. It does not replace the June record. A missing September observation is also different from a non-occurrence.

<a id="a-probability-is-more-than-a-yes-or-a-no"></a>

## A probability is more than a yes or a no

An event assigned probability 0.8 can fail to happen without logically contradicting the forecast. The remaining 0.2 is part of what was predicted. Yet a forecaster assigning 0.8 to everything should not be able to claim perpetual success by invoking that possibility after every failure.

Scoring makes the whole probability consequential. For a binary event with outcome $y\in\{0,1\}$, the Brier loss is:

$$
L_{\mathrm{Brier}}(p,y)=(p-y)^2.
$$

Lower is better. If the event happens, p = 0.8 receives loss 0.04 and p = 0.5 receives 0.25. If it does not happen, the losses are 0.64 and 0.25. Confidence creates both the possibility of a better score and a larger penalty for being wrong.

The logarithmic loss makes another trade-off:

$$
L_{\log}(p,y)=-y\log p-(1-y)\log(1-p).
$$

For an observed event use $-\log p$; for a non-event use $-\log(1-p)$. A certain prediction has zero loss if it is right and infinite loss if it is wrong. Assigning zero probability to an outcome that occurs is therefore penalised without bound. [Gneiting and Raftery's treatment of proper scoring rules](https://sites.stat.washington.edu/people/raftery/Research/PDF/Gneiting2007jasa.pdf) explains why a forecaster minimises its expected loss by reporting its assessed distribution honestly.

<a id="calibration-needs-resolution"></a>

## Calibration needs resolution

In a constructed ten-case example, forecasts consist of five assigned probability 0.8 and five assigned 0.2. Four events occur in the first group and one in the second. The observed frequencies equal the predicted probabilities in these small groups, and the mean Brier loss is 0.16. A constant 0.5 forecast on these same outcomes receives 0.25. The constant forecast gets the overall frequency right: five of ten events occurred. But it makes no distinction between cases. The varying probabilities preserve useful resolution while matching the group frequencies.

![All three calibration points match their group frequencies, but the varying forecast has mean Brier loss 0.16 against 0.25 for the constant forecast.](https://post-agi-economics.org/collections/thinking-gets-cheap/models-and-measures/a-forecast-meets-its-outcome/calibration-and-resolution.svg)

The counts belong beside the calibration points: there are only five cases in each varying-probability group, and ten in the constant comparison. These exact proportions explain the example; they do not estimate stable calibration from a large evaluation.

To judge calibration beyond this example, we need enough relevant cases and an account of their uncertainty and dependence. Ten forecasts about the same sector and overlapping quarter are not ten independent replications. A system can also score well overall while overestimating one group's prospects or failing on a changed operating condition. Which cases go wrong matters when someone uses the forecast.

<a id="the-alternative-can-be-very-simple"></a>

## The alternative can be very simple

A sophisticated timing model has to add information beyond a simpler comparator. For an adoption event, a baseline might use the previous observed rate or a predeclared trend. For a crossing time, it might use a fixed hazard under stated conditions. The baseline should be credible for the question, not intentionally bad. Both forecasts need the same event, origins, horizons and observations. One model predicting three months ahead cannot be compared casually with another updated the day before the outcome. Trying many model variants on a small evaluation window can also select a lucky winner. A rolling-origin comparison, in which each origin uses only prior information, makes the prospective test more faithful, though overlapping outcomes and structural change still affect its interpretation.

A forecast of the waiting time also has to account for incomplete observation. If the frontier has not been crossed by the end of observation, the waiting time is censored: it is known to exceed the observed interval, not to equal it. A score for a fully observed time cannot simply substitute the censoring date as an event date. Event-by-horizon probabilities remain one possible local target, provided the chosen horizons and observation rules are explicit.

<a id="a-changed-question-starts-another-comparison"></a>

## A changed question starts another comparison

Suppose the original target counted recurring operation, but a later survey counts any trial of an assistant. The measured series can rise even when recurring operation has not changed. [The counted event](https://post-agi-economics.org/collections/thinking-gets-cheap/models-and-measures/measuring-ai-diffusion/) has changed. It cannot be treated as a favourable outcome for the original forecast without a defensible bridge between definitions. A model update can legitimately improve future forecasts. A changed target can legitimately ask a better question. Keeping both histories distinct reveals what improved: the predictive method, the available information or the thing being predicted. It also reveals a forecast that no longer has a comparable outcome, rather than converting uncertainty into an automatic win.

A [local economic clock](https://post-agi-economics.org/blog/one-clock-many-frontiers/) gives a particular crossing a mathematical process. Its forecast then has to meet that process in public: definite enough to be scored, informative enough to beat a simpler account, and revisable without rewriting what it previously said. Trust accumulates through those encounters, not through the elegance of the countdown.


Reading path: [What breaks when thinking gets cheap](https://post-agi-economics.org/collections/thinking-gets-cheap/) > [Models and measures](https://post-agi-economics.org/collections/thinking-gets-cheap/models-and-measures/) > [A forecast meets its outcome](https://post-agi-economics.org/collections/thinking-gets-cheap/models-and-measures/a-forecast-meets-its-outcome/)
