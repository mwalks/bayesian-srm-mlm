# bayesian-srm-mlm
Snippets of final project for 8892.12 Applied Quantitative Methods in Anthropology II

A brief look into applications of Bayesian modeling to [common resource management experimental games](https://rdcu.be/ccoqV). Specifically, a cross-classified multi-level model and a bayesian social relations model (based on [work by Koster & Leckie](https://www.researchgate.net/publication/337800514_Statistical_Methods_and_Software_for_the_Multilevel_Social_Relations_Model)). I make use of McElreath's [Statistical Rethinking package](https://github.com/rmcelreath/rethinking/tree/Experimental) to compile RStan code.


The potential merits – and risks – of the practice of swidden agriculture, where farmers cultivate subsistence crops such as maize in patches of forests cleared by a process commonly known as “slash and burn,” have been widely debated across disciplines. Often, these discussions are focused on ascertaining whether swidden is inherently destructive of tropical forest environments (Malthus 1826; Boserup 1965), or whether it can exhibit sustainability.

Two predominant, opposing theories emerged as potential explanations for the complex functions of swidden agriculture: the first argues that swidden is strictly limited by ecological carrying capacity, or the maximum sustainable population size given the availability of resources, and therefore subjects natural environments to overexploitation and deforestation (Food and Agriculture Organization 1985); the second approach, contrary to ‘Western scientific’ management practices, conceives of ‘coupled human and natural systems’ in which human cultures develop detailed knowledge of their local environments and the processes which best conserve and protect this ecosystem – a collective understanding also known as Traditional Ecological Knowledge, or TEK. However, despite the significant corpora of research, which span questions about the integration of swidden in ecology, culture, society, and religion (Conklin 1954; Geertz 1963), how swidden can be practiced sustainably and augment forest resilience (Balée 2013), or even the role of swidden systems in a globalized, technological world (Weinstock 2015), the relationships between specific social and spatial dynamics and ecological features such as carrying capacities and stock effects remain unclear.

Despite the negative connotation of the phrase “slash and burn,” swidden agriculture is how many indigenous communities like the Q'eqchi Maya of southern Belize have been sustainably producing food for thousands of years.

There are a number of complex cultural and historical contexts which are needed to analyze the swidden practices of Q’eqchi’ Maya communities. Importantly, Q’eqchi’ social institutions do not actively protect common forest resources (Downey 2009). The resources are instead collectively managed through reciprocal exchanges of labor. This is a consequence of the colonial period when access to government land for swidden production – both subsistence and market-oriented – was largely unregulated, making land a common property resource available to Q’eqchi’ farmers (Downey 2015). In most villages, labor exchanges – which occur when one farmer asks a group of men to help with a difficult task such as planting or clearing the forest – have become the key social process involved with swidden agriculture (Wilk 1997). After each workgroup, a farmer is expected to close his debt to each man who helped him by reciprocating a day of labor.

The guiding research question here is: how do indigenous social norms like those surrounding this practice of common resource management help regulate the use of a natural resource such as the forest, making sure it remains sustainable (at a ‘group optimum’) rather than using it at its maximum rate (‘Nash equilibrium’; Nash 1950)? 

Our hypothesis is that social norms related to labor reciprocity encourage sustainable use of shared forest resources. 


We can trace various strategies of labor reciprocity such as graduated sanctioning by a simulated common resource management game. 

## The Milpa Game
The [game](https://rdcu.be/ccoqV) consists of a 10x10 board of “chips” representing forest resources. There are 3 Stages, each with 10 rounds. 5 players make requests each round that determine how much of the forest is cleared. After each Round, the forest regenerates an amount of chips proportional to how many 10s of chips are left:

Stages II and III are designed to explore the effect of helping and labor exchange. In Stage II, players require the assistance of the other group members to take more than 1 unit (players may always help themselves). The Nash equilibrium remains the same as in Stage I, as does the optimal group strategy, but there are numerous paths to success depending on how much help is given or withheld. 


In Stage III, there is a brief communication period in between rounds which players may use to discuss strategy. For the sake of this analysis, only Stage II will be used.

These data are well-suited for adapting a Bayesian approach due to the relatively small sample size and the complexity of the questions being asked. Regularizing priors and other features of Bayesian modeling will be essential to extracting various strategies being employed across rounds, such as graduated sanctioning. The data can also resemble a dyadic structure with player-requestor pairs for which the Bayesian social relations model would work well.

Some of the key questions these models can help answer are:

 - Can we isolate and trace different play strategies?
 - Do strategies change over time (rounds)?
 - Does reciprocity depend on previous help (lag)?
 - Does forest level determine request size?
