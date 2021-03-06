FAQ
===


My results are worse than the ones reported in the README, why?
---------------------------------------------------------------
There are few possibilities here:

1. Your data is wrong. We had this examples with wsj0-mix, WHAM etc..
where wv2 was used instead of wv1 to generate the data. This was fixed in
`#166 <https://github.com/mpariente/asteroid/pull/166>`_. Chances are there is a pretrained model available for the given dataset,
run the evaluation with it. If your results are different, it's a data problem.
Refs: `#164 <https://github.com/mpariente/asteroid/issues/164>`_,
`#165 <https://github.com/mpariente/asteroid/issues/165>`_ and `#188 <https://github.com/mpariente/asteroid/issues/188>`_.

2. You stopped training too early. We've seen this happen, specially with DPRNN.
Be sure that your training/validation losses are completely flat at the end of training.
Need to attach a DPRNN log here.

3. If it's not both, there is a real bug and we're happy you caught it!
Please, open an issue with your torch/pytorch_lightning/asteroid versions to let us know.

How long does it take to train a model?
---------------------------------------
Need a log here.

Can I use the pretrained models for commercial purposes?
--------------------------------------------------------
Not always. See the note on pretrained models Licenses :ref:`Note about licenses`
