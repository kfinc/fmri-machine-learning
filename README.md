# fmri-machine-learning
Learning/teaching materials on applying machine learning algorithms to fMRI data.

**What is machine learning?**

The art and science of giving computers the ability to learn to make decisions from data, whithout being explicitely programmed (DataCamp definition).

**How we can apply machine learning algorithms on fMRI data?**

With fMRI technique we can scan the human brain multiple times during performing some activity (e.g. task, rest, or sleep). Resulting brain images are stored in 4D arrays, where the first three dimensions are reserved for 3D brain image (so called *volume*), while remaining forth dimension represents time-point (one complete volume of the brain is aquired every 1-2 seconds), covering the whole scan time (usually 10-60 min).

Each brain volume includes thousands of voxels (3D pixels, commonly 1 $mm^{3}$ each). For purpose of running machine learning algorithms on fMRI data, we have to convert our 4D fMRI data into 2D array of features. To reduce the number of features, we can extract the brain activity from meaningful brain atlases, also known as *brain parcellatons*. For the instruction how to extract timeseries from brain parcellation check out this Nilearn [tutorial](https://nilearn.github.io/connectivity/functional_connectomes.html). 

In general we need something like this:
![](./figures/4d_to_2d.png)
Figure from Abraham et al.(2014)*Frontiers in Neuroinformatics* paper.

In this machine learning training materials I use previously prepared fMRI timeseries extracted from task and resting state data using [Schaefer](https://github.com/ThomasYeoLab/CBIG/tree/master/stable_projects/brain_parcellation/Schaefer2018_LocalGlobal) parcellation. I extracted timeseries from data of 10 subjects and concatenated to obtain long 2D array. 

In folder `data` you can find:
- prepared and concatenated fMRI timeseries for task and rest (`concat_10subjects_timeseries_shaefer400_pipeline-24HMP_8Phys_SpikeReg_4GS.npy`)
- table with timing of task conditions (`task_conditions.csv`)


