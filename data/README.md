Supplementary data  from Ider Chitham et al. 2020 - "Cosmological constraints from CODEX galaxy clusters spectroscopically confirmed by SDSS-IV/SPIDERS DR16"

# Cluster and member catalogues

* There are two different types of catalogues. **Cluster** catalogues and **member** catalogues. 

* To match the two types of catalogues, you must use the `mem_match_id`. The `id` column (in the member catalogue) is reserved for the member galaxies and defined by `objid + brickid * pow(2, 16) + release * pow(2, 40)` for the Legacy imaging surveys.

* The cluster catalogue is sorted by `lnlike` which is the total log-likelihood of the cluster. This is the sum of the cluster membership log-likelihood `lnlamlike` and the log-likelihood of the central galaxy `lncglike`. The reason for doing this, is because the total log-likelihood is what is maximised when `redmapper` is run in scanning mode and it is also used to rank clusters during the percolation process.

* There are several different versions of the cluster redshift (and uncertainties) in the catalogue. Here they are listed in descending order of recommended usage:

* best_z - Best available cluster redshift
* spec_z_boot - Bootstrap estimate of spectroscopic redshift
* cg_spec_z - Spectroscopic redshift of central galaxy
* photo_z - Best photometric cluster redshift

The method of assigning spectroscopic redshifts is inherited directly from the SPIDERS automated cluster redshift pipeline. For the details please refer to [Clerc et al. 2016](http://adsabs.harvard.edu/abs/2016MNRAS.463.4490C) section 4.3 "Automatic membership" and 4.5 "Redshift and velocity dispersion estimates".

## Cluster Column Description

```
TTYPE1  = 'mem_match_id'           / label for column 1\
TCOMM1  = 'Numerical Cluster ID. Use to match to member catalogue'\
--
TTYPE2  = 'ra_opt  '           / label for column 2\
TCOMM2  = 'Right Ascension of optical centre'\
--
TTYPE3  = 'dec_opt '           / label for column 3\
TCOMM3  = 'Declination of optical centre'\
--
TTYPE4  = 'ra_xray '           / label for column 4\
TCOMM4  = 'Right Ascension of X-ray prior'\
--
TTYPE5  = 'dec_xray'           / label for column 5\
TCOMM5  = 'Declination of X-ray prior'\
--
TTYPE6  = 'hpix    '           / label for column 6\
TCOMM6  = 'Healpix index nside=32 and nest=False'\
--
TTYPE7  = 'refmag  '           / label for column 7\
TCOMM7  = 'Apparent reference band magnitude of central galaxy'\
--
TTYPE8  = 'refmag_err'         / label for column 8\
TCOMM8  = 'Apparent reference band magnitude error of central galaxy'\
--
TTYPE9  = 'lambda  '           / label for column 9\
TCOMM9  = 'Optical richness'\
--
TTYPE10 = 'lambda_e'           / label for column 10\
TCOMM10 = 'Optical richness uncertainty'\
--
TTYPE11 = 'z_lambda'           / label for column 11\
TCOMM11 = 'Uncorrected cluster photometric redshift'\
--\
TTYPE12 = 'z_lambda_e'         / label for column 12\
TCOMM12 = 'Uncorrected cluster photometric redshift uncertainty'\
--\
TTYPE13 = 'r_lambda'           / label for column 13\
TCOMM13 = 'Richness dependant redmapper radius (Mpc)'\
--\
TTYPE14 = 'scaleval'           / label for column 14\
TCOMM14 = 'Richness scale factor Eq. 2 of Rykoff 2016'\
--\
TTYPE15 = 'maskfrac'           / label for column 15\
TCOMM15 = 'Fraction of cluster area which is masked'\
--\
TTYPE16 = 'ebv_mean'           / label for column 16\
TCOMM16 = 'Mean ebv value'\
--\
TTYPE17 = 'lnlamlike'          / label for column 17\
TCOMM17 = 'Cluster member likelihood'\
--\
TTYPE18 = 'lncglike'           / label for column 18\
TCOMM18 = 'Central likelihood'\
--\
TTYPE19 = 'lnlike  '           / label for column 19\
TCOMM19 = 'Total cluster likelihood (lnlamlike + lncglike)'\
--\
TTYPE20 = 'lim_exptime'        / label for column 20\
TCOMM20 = 'Median exposure time from maskgals'\
--\
TTYPE21 = 'lim_limmag'         / label for column 21\
TCOMM21 = 'Median magnitude limit from maskgals'\
--\
TTYPE22 = 'lambda_c'           / label for column 22\
TCOMM22 = 'Optical richness averaged over the most likely centres'\
--\
TTYPE23 = 'lambda_ce'          / label for column 23\
TCOMM23 = 'Uncertainty on optical richness averaged over the most likely &'\
--\
TTYPE24 = 'mag     '           / label for column 24\
TCOMM24 = 'Apparent magnitude of central galaxy in each band'\
--\
TTYPE25 = 'mag_err '           / label for column 25\
TCOMM25 = 'Apparent magnitude error of central galaxy in each band'\
--\
TTYPE26 = 'pzbins  '           / label for column 26\
TCOMM26 = 'Redshift points at which P(z) is evaluated'\
--\
TTYPE27 = 'pz      '           / label for column 27\
TCOMM27 = 'P(z) evaluated at redshift points given by pzbins'\
--\
TTYPE28 = 'ra_cent '           / label for column 28\
TCOMM28 = 'Right Ascension of the most likely central candidates'\
--\
TTYPE29 = 'dec_cent'           / label for column 29\
TCOMM29 = 'Declination of the most likely central candidates'\
--\
TTYPE30 = 'id_cent '           / label for column 30\
TCOMM30 = 'Galaxy ID of the most likely central candidates'\
--\
TTYPE31 = 'lambda_cent'        / label for column 31\
TCOMM31 = 'Optical richness at the position of most likely central candidates'\
--\
TTYPE32 = 'zlambda_cent'       / label for column 32\
TCOMM32 = 'Uncorrected photometric redshift at the position of most likely &'\
--\
TTYPE33 = 'p_cen   '           / label for column 33\
TCOMM33 = 'Centring probability of the most likely central candidates'\
--\
TTYPE34 = 'best_z  '           / label for column 34\
TCOMM34 = 'Best available cluster redshift'\
--\
TTYPE35 = 'spec_z_boot'        / label for column 35\
TCOMM35 = 'Bootstrap estimate of spectroscopic cluster redshift'\
--\
TTYPE36 = 'spec_z  '           / label for column 36\
TCOMM36 = 'Spectroscopic cluster redshift'\
--\
TTYPE37 = 'cg_spec_z'          / label for column 37\
TCOMM37 = 'Spectroscopic redshift of central galaxy'\
--\
TTYPE38 = 'photo_z '           / label for column 38\
TCOMM38 = 'Best photometric cluster redshift'\
--\
TTYPE39 = 'photo_zerr'         / label for column 39\
TCOMM39 = 'Error on best photometric cluster redshift'\
```

##  Member Column Description

```
TTYPE1  = 'mem_match_id'           / label for column 1\
TCOMM1  = 'Numerical Cluster ID. Use to match to cluster catalogue'\
--
TTYPE2  = 'id      '           / label for column 2\
TCOMM2  = 'Galaxy ID: objid + brickid * pow(2, 16) + release * pow(2, 40)'\
--
TTYPE3  = 'ra      '           / label for column 3\
TCOMM3  = 'Right Ascension of galaxy'\
--
TTYPE4  = 'dec     '           / label for column 4\
TCOMM4  = 'Declination of galaxy'\
--
TTYPE5  = 'r       '           / label for column 5\
TCOMM5  = 'Radius from cluster centre'\
--
TTYPE6  = 'p       '           / label for column 6\
TCOMM6  = 'Membership probability'\
--
TTYPE7  = 'pfree   '           / label for column 7\
TCOMM7  = 'Probability that member is not a member of a higher ranked cluster'\
--
TTYPE8  = 'pcol    '           / label for column 8\
TCOMM8  = 'Probability of membership using color/luminosity'\
--
TTYPE9  = 'theta_i '           / label for column 9\
TCOMM9  = 'Luminosity weight'\
--
TTYPE10 = 'theta_r '           / label for column 10\
TCOMM10 = 'Radial weight'\
--
TTYPE11 = 'refmag  '           / label for column 11\
TCOMM11 = 'Apparent reference band magnitude'\
--
TTYPE12 = 'refmag_err'         / label for column 12\
TCOMM12 = 'Apparent reference band magnitude error'\
--
TTYPE13 = 'zred    '           / label for column 13\
TCOMM13 = 'Photometric galaxy redshift'\
--
TTYPE14 = 'zred_e  '           / label for column 14\
TCOMM14 = 'Error on photometric galaxy redshift'\
--
TTYPE15 = 'zred_chisq'         / label for column 15\
TCOMM15 = 'Photometric redshift fit quality'\
--
TTYPE16 = 'chisq   '           / label for column 16\
TCOMM16 = 'Multicolor filter. Eq. 6 of Rykoff 2014'\
--
TTYPE17 = 'ebv     '           / label for column 17\
TCOMM17 = 'ebv     '\
--
TTYPE18 = 'zspec   '           / label for column 18\
TCOMM18 = 'Spectroscopic redshift'\
--
TTYPE19 = 'mag     '           / label for column 19\
TCOMM19 = 'Apparent magnitude in each band'\
--
TTYPE20 = 'mag_err '           / label for column 20\
TCOMM20 = 'Apparent magnitude error in each band'\
--
TTYPE21 = 'dcent_opt'          / label for column 21\
TCOMM21 = 'Distance to optical cluster centre (Mpc)'\
--
TTYPE22 = 'dcent_xray'         / label for column 22\
TCOMM22 = 'Distance to X-ray cluster centre (Mpc)'\
```
