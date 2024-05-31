# Causal-Discovery-for-Business-Processes

This repository contains experiments described in the paper *Data-Driven Decision Support for Business Processes: Causal Reasoning and Discovery* by Ali J. Alaee, Mathias Weidlich, and Arik Senderovich.

## File Descriptions

**DataGenerator_mainprocess.ipynb**  
This notebook generates a synthetic dataset for the main process example provided in the paper. Based on the causal graph in Fig. 2, it creates 10,000 samples, converts them into a trace log, and finally into an event log. The resulting .csv file can be used with the Bayesys causal discovery tool to identify the underlying causal graph. Additionally, the event log can be used with the Inductive Miner to discover the process map.

**BPI2012_TabularData_Extraction.ipynb**  
This notebook extracts a tabular dataset of decisions and contextual variables from the real-world BPI Challenge 2012 dataset. The output .csv file can be used with the Bayesys causal discovery tool to identify the underlying causal graph.

**ATE_calculation.ipynb**  
This notebook facilitates the calculation of Average Treatment Effects (ATE) and Conditional Average Treatment Effects (CATE) using do-calculus. It requires an input causal graph and a .csv dataset.


##Abstract of the paper

Various types of decisions influence the execution of a busi- MW, update once
intro is doneness process, e.g., in terms of control-flow and resource assignments. Data
recorded during process execution can be used to identify which decisions
are informed by data and by previous decisions, to predict their outcome,
and to guide interventions as part of a what-if analysis. The latter requires
causal models that explain decisions. Yet, existing causal techniques for
business processes are limited: they focus on control-flow decisions only,
ignore confounding variables, and use ad-hoc methods to resolve causal
conflicts. In this paper, we fill this gap, by introducing a business pro-
cess causal decision model (BP-CDM) that generalizes existing models
for decision support. It incorporates data variables, which uncover con-
founding effects, and capture resource decisions. Moreover, we provide
a general causal discovery algorithm, based on the notion of temporal
tiers, that takes process precedence into account, without the need for
ad-hoc conflict resolution mechanisms. We demonstrate the usefulness of
our approach through experiments with synthetically generated datasets.
