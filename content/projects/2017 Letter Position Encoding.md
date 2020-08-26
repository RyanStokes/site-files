+++
author = "Ryan Stokes"
title = "Letter Position Encoding"
date = "2017-01-01"
description = ""

categories = [
    "cognitive science",
]
+++

## Abstract

Visual word recognition requires the identification
of a word’s component letters as well as their position within a
word. The position of letters, once thought to be coded to the
precise location in a word, is now understood to be more flexible.
Indeed, a wealth of experimental evidence supports a view of
visual word recognition that is forgiving to local changes in the
position of letters. We present a model of letter position encoding,
as an extension of the Overlap model, that treats letters as
distributions along a normalized retinotopic space. Additionally,
letters that do not belong in a target word, or are distant from
the expected location, are modeled to inhibit the activation of the
target word. This method has not yet been explored in the letter
position encoding literature, and can help increase the biological
plausibility of these models. We show that model estimates fit
well with a database of priming studies used to investigate the
effects of letter position manipulations on participants’ reaction
time and accuracy.

## Findings

Our model of letter position encoding is informed by the
various phenomenon reported by masked priming studies, and
also constrained by the limitations of biological plausibility.
Transposition effects, relative position effects, letter inhibition,
and letter migration effects are each explained by the model
using a simple network of neurons and two free parameters.
Transposition effects are explained at the letter layer. Adjacent letters have overlapping letter distributions that maintain
some level of activation if those letters are transposed. However, distant letter transpositions will have inhibitory effects 
on word activation. This is because letter identification follows
an activation gradient with the most activation centered around
the true position of the letter, and inhibitory weights set near
the tails. The model’s prediction is consistent with behavioral
studies where transpositions of more than two letter spaces
have small priming effects on target words [26], [12].
Words with letters that have been removed (subset) or
inserted (superset) will still generate reliable priming effects
[26]. A shared space must then exist between words of
different lengths for which comparisons can be made. The
model accomplishes this by mapping every word onto the same
normalized space, independent of the number of neurons in
the letter layer. This strategy appears to be effective up to two
letters of removal or insertion as the model underestimated
performance of the half word (123/456) condition.
Letter migration effects can be informally evaluated by allowing the network to accept inputs from multiple letters at the
same position. Two words can then be presented to the network
at the same time, similar to an experiment where a word is
presented to either side of the screen. This activates both sets
of letters at overlapping positions. As expected, the lexical
units for each of the two words will increase in activation,
but occasionally, words which contain a combination of letters
from the first two words will also activate strongly. The model
is naturally flexible to letter position between words as well,
eliciting strong activation for stop when presented with step
and soap together. Currently, the model does well to fit commonly studied
masked priming effects. However, there are several simplifications that prevent the network from explaining specific
types of conditions. For instance, the model has nothing to
say about the initial letter position effect, where the first letter
will be identified more quickly and accurately than other letters
during a forced choice task. It is straightforward to include an
additional parameter to increase activation of the initial letter,
but this approach seems simplistic and unnatural. Instead,
a model of attention that is integrated into the network is
necessary to identify a word shape, and increase activation to
the appropriate letter positions. This extension would fit more
accurately with current theories of initial letter position effects
[18]. Additional improvements, such as phonology, semantics,
and syllable boundaries can also improve the explanatory
power of the network and will likely be included in further
iterations. The current model can most effectively be used as a
front-end of letter position encoding in more advanced models
of visual word recognition.

## Paper

[Letter Position Encoding in a Neural Framework](/images/Letter Position Encoding/Stokes2017.pdf)