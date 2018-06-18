This repo contains R code to process physiology and growth data from a container volume sink limited experiment at Western Sydney University and later use data assimilation (DA) technique to infer the C mass balances from the processed measurements. The R script "CentralScript.R" replicates the figures and analyses presented in the following manuscript:
"Inferring the effects of sink strength on plant carbon balance from experimental measurements" by Kashif Mahmud, Belinda Medlyn, Remko Duursma, Courtney Campany, Martin De Kauwe.

***Please note simulating Carbon Dynamic Model (CDM) takes significant computational times due to running the DA framework several times. This can take long time (~30 minutes) to run all 7 simulations in parallel using 7 CPU cores on a 2.5 GHz Intel Core i7 Macbook Pro. 

We infer a comprehensive suite of empirical photosynthesis vs. growth allocation patterns for an Australian woody plant seedling under belowground sink limited condition, by applying a novel DA framework to data from this experiment, mining the existing data to generate substantial new information about the C dynamics in plants. The method uses a new mass balance approach to infer the rate and timing of the transfer of photosynthate to plant growth via storage pool, with exploring the belowground sink manipulation.

To use this code, I recommend that you clone this repository into an Rstudio project by copying the SSH (or HTTPS) link on the right, and pasting the link into a new Rstudio project URL (File > New Project > Version Control > Git). You will also need git. This process is described in useful detail here: http://www.molecularecologist.com/2013/11/using-github-with-r-and-rstudio/. The code within "CentralScript.R" will download all of the raw data from figshare, place them in the "raw_data" folder, then pre-process the raw data to fit the DA framework (which are also stored in the "processed_data" folder), and recreate all of the figures and tables in the "output" folder. Send Kashif an e-mail if you have trouble, and I will try to help you out (k.mahmud@westernsydney.edu.au).

Experimental details:
This folder consists of existing dataset from the container volume experiment which was carried out at the Hawkesbury Forest Experiment site (33°37'S 150°44'E) in Richmond, NSW, Australia. The site and experimental setup have been explained in detail by Campany et al. (2017). In brief, 20 weeks old Eucalyptus tereticornis seedlings in tube stock were chosen from a single local Cumberland plain cohort. Ten additional seedlings of similar age and growth were harvested to measure initial leaf area and dry mass of leaves, stems and roots. A total of 49 Eucalyptus tereticornis seedlings were grown in a range of container sizes (5 L to 35 L) in field conditions, using freely-rooted seedlings as a control for the container size treatments, with the goal to examine how the C balance of the plants are affected to belowground sink limitations. Six container sizes were used with each container experiment had a complete replicate set of six container volumes along with a free seedling. Similar notations are used here as Campany et al. (2017) for the treatments in different pots as 5 L, 10 L, 15 L, 20 L, 25 L and 35 L in respect of their pot sizes. The experiment tracked leaf-level gas exchange, leaf carbohydrate accumulation and seedling allometry over the course of 4 months for all 7 treatments. 
