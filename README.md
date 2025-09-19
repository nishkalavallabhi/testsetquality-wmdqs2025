# Annotated Data for "Test Set Quality in Multilingual LLM Evaluation"

This repo contains data that was annotated for the paper [Test Set
Quality in Multilingual LLM
Evaluation](https://arxiv.org/abs/2508.02635). The goal of this
project was to identify errors in benchmark datasets in French and
Telugu, in order to investigate how LLM performance would be impacted
if we removed erroneous samples from the test data.

## Usage

The three datasets are in comma-separate value (CSV) format, encoded
in UTF-8.

The annotations include coarse-grained "concerns" and finer-grained
error types. The latter were created after the former to reflect how
the annotators interpreted and refined the more coarse-grained
"concerns" that were defined for the annotation task.

To look into the errors identified in the French dataset, use the
columns "Consensus" (for the concerns) and "Fine error types". For the
two Telugu datasets, use the columns "concerns-A" and "concerns-B" (as
consensus deliberation was not conducted on these datasets), as well
as "Fine error types".

To reproduce our experiments on LLM evaluation in French, filter out
all samples except those where the value in the "Consensus" column is
"NoConcerns". For Telugu, filter out all samples except those where
BOTH "concerns-A" and "concerns-B" contain the value "NoConcerns".
