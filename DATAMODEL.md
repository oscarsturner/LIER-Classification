## Data Model: MaNGA Ionization Morphology Classifications

### General Description
These are classifications of 10,451 MaNGA observations based on the distribution of ionization in the target galaxy. The ionization of each spaxel is classified as Seyfert, star-forming, or low-ionization emission using the ionized sulfur BPT diagram. Galaxies are classified as Seyfert galaxies, star-forming galaxies, central low-ionization emission region galaxies (cLIERs), extended low-ionization emission region galaxies (eLIERs), galaxies with outer or extraplanar low-ionization emission regions (outLIERs), mergers, and unclassifiable (lineless). The table also contains information on the ionization morphology of the galaxy, including the last LIER radius, a flag for any Seyfert regions, and a radial ionization profile with 10 bins. Also included is helpful information such as mass estimates, an inclination angle estimate, and magnitude measurements from the NASA-Sloan Atlas. 

### Columns
**mangaid** and **plateifu** are the MaNGA ID of the target galaxy and the plateifu for the observation. 
**ewha_1re** contains the mean equivalent width of the H alpha line in angstroms in a circle of radius 1 effective radius around the central spaxel of the observation. 
**classification** is the object's ionization morphology classification. Options: 'SF', 'cLIER', 'eLIER', 'Sy', 'Merger', 'Lineless', 'Bad_SNR (Lineless)'. 
**classification_in_1psf** and **classification_out_1psf** are the classifications for the ionization inside and outside a circle of 1 PSF centered around the central spaxel of the observation. Options: 'SF', 'LIER', 'Sy', 'Merger', 'Lineless', 'Bad_SNR (Lineless)'
**last_lier_re** contains the median Re of the farthest bin in the radial profile classified as having LIER-like emission. 
**sy_annulus_flag** is True if a radial profile of the galaxy _with a signal-to-noise ratio cutoff of either 2 or 3_ contains a bin classified as having Seyfert emission. 
**baseline_radial_profile** contains, for classifiable galaxies (i.e. not mergers or lineless), a 10-bin radial profile of the ionization within 10 evenly radially wide annuli, out to the farthest classifiable spaxel of the galaxy. 
**log_sersic_mass, log_elpetro_mass, phi,** and **nsa_sersic_absmag (FNugriz)** contain, respectively, a stellar mass estimate using a sersic fit of the galaxy; a stellar mass estimate using an elliptical profile; the inclination angle of the galaxy, and magnitude estimates in the 7 SDSS color bands. These measurements are taken from the MaNGA drpall and are included in the table for convenience. 
