# Category Group diffrn_data_set_group


              Categories extending the description of measured diffraction data.

---

## Category pdbx_diffrn_data_section


              The pdbx_diffrn_data_section category records the contents of a diffraction
              data section.

---


```
     
     #
      _pdbx_diffrn_data_section.id              'ds-merged-1'
      _pdbx_diffrn_data_section.type_scattering 'x-ray'
      _pdbx_diffrn_data_section.type_merged     'true'
      _pdbx_diffrn_data_section.type_scaled     'true'
      _pdbx_diffrn_data_section.details         'Optional details describing this example diffraction data section'
     
```


---

| Attribute | Key | Required | Type | Units | Enumerated | Bounded |
| --------- | --- | -------- | ---- | ----- | ---------- | ------- |
| details | no | no | text | None | no | no |
| id | yes | yes | code | None | no | no |
| type_merged | no | yes | code | None | yes | no |
| type_scaled | no | yes | code | None | yes | no |
| type_scattering | no | yes | code | None | yes | no |

---

#### _pdbx_diffrn_data_section.details


      Additional details describing the contents of the diffraction data set.



#### _pdbx_diffrn_data_section.id (key)


      The value of _pdbx_diffrn_data_section.id uniquely identifies a data section.



#### _pdbx_diffrn_data_section.type_merged (required)


      A flag to indicate merged diffraction data.



---

| Allowed Values | Detail |
| -------------- | ------ |
| false |   |
| true |   |


#### _pdbx_diffrn_data_section.type_scaled (required)


      A flag to indicate scaled diffraction data.



---

| Allowed Values | Detail |
| -------------- | ------ |
| false |   |
| true |   |


#### _pdbx_diffrn_data_section.type_scattering (required)


      The diffraction scattering type.



---

| Allowed Values | Detail |
| -------------- | ------ |
| electron |   |
| neutron |   |
| x-ray |   |


## Category pdbx_diffrn_data_section_contents


              The pdbx_diffrn_data_section_contents category records the correspondences
              between diffraction data sets references in PDB coordinate entry files and
              the data sections diffraction data files.


---


```
     
         #
         #
         loop_
         _pdbx_diffrn_data_section_contents.data_section_id
         _pdbx_diffrn_data_section_contents.content_type
         'ds-merged-1'   'X-ray structure factor amplitudes'
         'ds-merged-1'   'X-ray calculated amplitudes'
```


---

| Attribute | Key | Required | Type | Units | Enumerated | Bounded |
| --------- | --- | -------- | ---- | ----- | ---------- | ------- |
| content_type | yes | yes | line | None | yes | no |
| data_section_id | yes | yes | code | None | no | no |

---

#### _pdbx_diffrn_data_section_contents.content_type (key)


      The value of _pdbx_diffrn_data_section_contents.content_type uniquely identifies
      a data section in a diffraction data file.



---

| Allowed Values | Detail |
| -------------- | ------ |
| Electron structure factor amplitudes |   |
| Neutron structure factor amplitudes |   |
| X-ray 2FO-FC map coeff |   |
| X-ray 2FOFC map coefficients |   |
| X-ray FEM map coeff |   |
| X-ray FO-FC map coeff |   |
| X-ray FOM, X-ray batch flag from mtz |   |
| X-ray R-free set flag |   |
| X-ray calculated amplitudes |   |
| X-ray calculated phases |   |
| X-ray density modified experimental phases |   |
| X-ray experimental phases |   |
| X-ray intensity(+) |   |
| X-ray intensity(-) |   |
| X-ray structure factor amplitudes |   |
| X-ray structure factor intensities, unmerged |   |
| X-ray unmerged intensities |   |


#### _pdbx_diffrn_data_section_contents.data_section_id (key)


      The value of _pdbx_diffrn_data_section_contents.data_section_id uniquely identifies
      a data section in a diffraction data file.



## Category pdbx_diffrn_data_section_correspondence


              The pdbx_diffrn_data_section_correspondence category records the correspondences
              between diffraction data sets references in PDB coordinate entry files and
              the data sections diffraction data files.


---


```
     
         #
          loop_
         _pdbx_diffrn_data_section_correspondence.diffrn_id
         _pdbx_diffrn_data_section_correspondence.data_section_id
         1 'ds-merged-1'
```


---

| Attribute | Key | Required | Type | Units | Enumerated | Bounded |
| --------- | --- | -------- | ---- | ----- | ---------- | ------- |
| data_section_id | yes | yes | code | None | no | no |
| diffrn_id | yes | yes | code | None | no | no |

---

#### _pdbx_diffrn_data_section_correspondence.data_section_id (key)


      The value of _pdbx_diffrn_data_section_correspondence.data_section_id uniquely identifies
      a data section in a diffraction data file.



#### _pdbx_diffrn_data_section_correspondence.diffrn_id (key)


      The value of _pdbx_diffrn_data_section_correspondence.diffrn_id uniquely identifies
      a diffraction data set in a PDB coordinate model data file.



## Category pdbx_diffrn_data_section_experiment


              The pdbx_diffrn_data_section_experiment category records an admin
              of the parent or primary data sections contributing to the contents to
              a target data section.


---


```
     
      loop_
      _pdbx_diffrn_data_section_experiment.ordinal
      _pdbx_diffrn_data_section_experiment.data_section_id
      _pdbx_diffrn_data_section_experiment.proposal_id
       1 'ds-unmerged-1' 1234A
```


---

| Attribute | Key | Required | Type | Units | Enumerated | Bounded |
| --------- | --- | -------- | ---- | ----- | ---------- | ------- |
| data_section_id | yes | yes | code | None | no | no |
| details | no | no | line | None | no | no |
| ordinal | yes | yes | int | None | no | no |
| proposal_id | no | no | line | None | no | no |

---

#### _pdbx_diffrn_data_section_experiment.data_section_id (key)


      The value of data_set_id uniquely identifies a data section.



#### _pdbx_diffrn_data_section_experiment.details


      A description of any additional details with the data collection



#### _pdbx_diffrn_data_section_experiment.ordinal (key)


      Ordinal index for the admin section.



#### _pdbx_diffrn_data_section_experiment.proposal_id


      A site specific 'proposal' identifier for this dataset.



## Category pdbx_diffrn_data_section_index


              The pdbx_diffrn_data_section_index category records an index
              of the parent or primary data sections contributing to the contents to
              a target data section.


---


```
     
      loop_
      _pdbx_diffrn_data_section_index.data_section_id
      _pdbx_diffrn_data_section_index.parent_data_section_id
      'ds-merged-1'  ds-unmerged-1'
      'ds-merged-1'  ds-unmerged-2'
```


---

| Attribute | Key | Required | Type | Units | Enumerated | Bounded |
| --------- | --- | -------- | ---- | ----- | ---------- | ------- |
| data_section_id | yes | yes | code | None | no | no |
| parent_data_section_id | yes | yes | code | None | no | no |

---

#### _pdbx_diffrn_data_section_index.data_section_id (key)


      The value of data_set_id uniquely identifies a data section.



#### _pdbx_diffrn_data_section_index.parent_data_section_id (key)


      The value of parent_data_set_id identifies a parent or contributing data section.



## Category pdbx_diffrn_data_section_site


              This pdbx_diffrn_data_section_site category records the site that data collection occured.

---


```
     
      loop_
      _pdbx_diffrn_data_section_site.data_section_id
      _pdbx_diffrn_data_section_site.facility
      _pdbx_diffrn_data_section_site.beamline
      _pdbx_diffrn_data_section_site.collection_date
      _pdbx_diffrn_data_section_site.detector
      _pdbx_diffrn_data_section_site.detector_type
       'ds-unmerged-1' APS 14-BM-C 2016-09-11 'ADSC QUANTUM 315' CCD
```


---

| Attribute | Key | Required | Type | Units | Enumerated | Bounded |
| --------- | --- | -------- | ---- | ----- | ---------- | ------- |
| beamline | no | no | line | None | yes | no |
| collection_date | no | no | yyyy-mm-dd:hh:mm-flex | None | no | no |
| data_section_id | yes | yes | code | None | no | no |
| detector | no | no | line | None | yes | no |
| detector_type | no | no | line | None | yes | no |
| facility | no | no | line | None | yes | no |

---

#### _pdbx_diffrn_data_section_site.beamline


      For a non-home source, the beamline or sector where data collection took place



---

| Allowed Values | Detail |
| -------------- | ------ |
| 14-BM-C |   |
| 14.1 |   |
| X25 |   |


#### _pdbx_diffrn_data_section_site.collection_date


      The date that data collection starts



#### _pdbx_diffrn_data_section_site.data_section_id (key)


      The value of data_set_id uniquely identifies a data section.



#### _pdbx_diffrn_data_section_site.detector


       Detector used for data collection



---

| Allowed Values | Detail |
| -------------- | ------ |
| ADSC QUANTUM 315 |   |


#### _pdbx_diffrn_data_section_site.detector_type


       Detector type used for data collection



---

| Allowed Values | Detail |
| -------------- | ------ |
| CCD |   |
| CMOS |   |
| PIXEL |   |


#### _pdbx_diffrn_data_section_site.facility


      If a non-home source is used for data collection, the facility housing the equipment



---

| Allowed Values | Detail |
| -------------- | ------ |
| ALBA |   |
| ALS |   |
| APS |   |
| AichiSR |   |


## Category pdbx_diffrn_image_proc


               Data items in the pdbx_diffrn_image_proc category record details of
               image data processing transformations.

---


```
     
         loop_
         _pdbx_diffrn_image_proc.image_id
         _pdbx_diffrn_image_proc.crystal_id
         _pdbx_diffrn_image_proc.image_number
         _pdbx_diffrn_image_proc.phi_value
         _pdbx_diffrn_image_proc.wavelength
         _pdbx_diffrn_image_proc.cell_length_a
         _pdbx_diffrn_image_proc.cell_length_b
         _pdbx_diffrn_image_proc.cell_length_c
         _pdbx_diffrn_image_proc.cell_angle_alpha
         _pdbx_diffrn_image_proc.cell_angle_beta
         _pdbx_diffrn_image_proc.cell_angle_gamma
         1  1  1  0.5000  0.91837  51.3940 109.0130 137.3070 90.000 90.000 90.000
         1  2  1  0.6000  0.91837  51.3940 109.0130 137.3070 90.000 90.000 90.000
         # ...  abbreviated ...
     
```


---

| Attribute | Key | Required | Type | Units | Enumerated | Bounded |
| --------- | --- | -------- | ---- | ----- | ---------- | ------- |
| cell_angle_alpha | no | no | float | degrees | no | yes |
| cell_angle_beta | no | no | float | degrees | no | yes |
| cell_angle_gamma | no | no | float | degrees | no | yes |
| cell_length_a | no | no | float | angstroms | no | yes |
| cell_length_b | no | no | float | angstroms | no | yes |
| cell_length_c | no | no | float | angstroms | no | yes |
| crystal_id | yes | yes | int | None | no | no |
| image_id | yes | yes | int | None | no | no |
| image_number | no | no | int | None | no | no |
| phi_value | no | yes | float | None | no | no |
| wavelength | no | yes | float | angstroms | no | yes |

---

#### _pdbx_diffrn_image_proc.cell_angle_alpha


               Unit-cell angle alpha in degrees.



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0.0 | 180.0 |


#### _pdbx_diffrn_image_proc.cell_angle_beta


               Unit-cell angle beta in degrees.



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0.0 | 180.0 |


#### _pdbx_diffrn_image_proc.cell_angle_gamma


               Unit-cell angle gamma in degrees.



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0.0 | 180.0 |


#### _pdbx_diffrn_image_proc.cell_length_a


               Unit-cell length a in angstroms.



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0.0 | <h3>+&infin;</h3> |


#### _pdbx_diffrn_image_proc.cell_length_b


               Unit-cell length b reported in angstroms.



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0.0 | <h3>+&infin;</h3> |


#### _pdbx_diffrn_image_proc.cell_length_c


               Unit-cell length c reported in angstroms.



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0.0 | <h3>+&infin;</h3> |


#### _pdbx_diffrn_image_proc.crystal_id (key)


      The value of crystal_id uniquely identifies a crystal sample within a data section.



#### _pdbx_diffrn_image_proc.image_id (key)


      The value of image_id uniquely identifies a location (spot) on a crystal sample.



#### _pdbx_diffrn_image_proc.image_number


      The value of image_number identifies a collection of reflection measurements.



#### _pdbx_diffrn_image_proc.phi_value (required)


               The interpolation value.



#### _pdbx_diffrn_image_proc.wavelength (required)


               The radiation wavelength in angstroms.



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0.0 | <h3>+&infin;</h3> |


## Category pdbx_diffrn_merged_cell


               Data items in the pdbx_diffrn_merged_cell category record details about the
               crystallographic cell parameters for this merged data set

---


```
     
      _pdbx_diffrn_merged_cell.data_section_id   'ds-merged-1'
      _pdbx_diffrn_merged_cell.cell_length_a      51.3940
      _pdbx_diffrn_merged_cell.cell_length_b     109.0130
      _pdbx_diffrn_merged_cell.cell_length_c     137.3070
      _pdbx_diffrn_merged_cell.cell_angle_alpha   90.0000
      _pdbx_diffrn_merged_cell.cell_angle_beta    90.0000
      _pdbx_diffrn_merged_cell.cell_angle_gamma   90.0000
     
```


---

| Attribute | Key | Required | Type | Units | Enumerated | Bounded |
| --------- | --- | -------- | ---- | ----- | ---------- | ------- |
| cell_angle_alpha | no | no | float | degrees | no | yes |
| cell_angle_beta | no | no | float | degrees | no | yes |
| cell_angle_gamma | no | no | float | degrees | no | yes |
| cell_length_a | no | no | float | angstroms | no | yes |
| cell_length_b | no | no | float | angstroms | no | yes |
| cell_length_c | no | no | float | angstroms | no | yes |
| cell_volume | no | no | float | angstroms_cubed | no | yes |
| data_section_id | yes | yes | code | None | no | no |

---

#### _pdbx_diffrn_merged_cell.cell_angle_alpha


               Unit-cell angle alpha in degrees.



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0.0 | 180.0 |


#### _pdbx_diffrn_merged_cell.cell_angle_beta


               Unit-cell angle beta in degrees.



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0.0 | 180.0 |


#### _pdbx_diffrn_merged_cell.cell_angle_gamma


               Unit-cell angle gamma in degrees.



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0.0 | 180.0 |


#### _pdbx_diffrn_merged_cell.cell_length_a


               Unit-cell length a in angstroms.



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0.0 | <h3>+&infin;</h3> |


#### _pdbx_diffrn_merged_cell.cell_length_b


               Unit-cell length b reported in angstroms.



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0.0 | <h3>+&infin;</h3> |


#### _pdbx_diffrn_merged_cell.cell_length_c


               Unit-cell length c reported in angstroms.



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0.0 | <h3>+&infin;</h3> |


#### _pdbx_diffrn_merged_cell.cell_volume


               Cell volume V in angstroms cubed.

               V = a b c (1 - cos^2^~alpha~ - cos^2^~beta~ - cos^2^~gamma~
                          + 2 cos~alpha~ cos~beta~ cos~gamma~)^1/2^

               a     = _pdbx_diffrn_merged_cell.cell_length_a
               b     = _pdbx_diffrn_merged_cell.cell_length_b
               c     = _pdbx_diffrn_merged_cell.cell_length_c
               alpha = _pdbx_diffrn_merged_cell.cell_angle_alpha
               beta  = _pdbx_diffrn_merged_cell.cell_angle_beta
               gamma = _pdbx_diffrn_merged_cell.cell_angle_gamma



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0.0 | <h3>+&infin;</h3> |


#### _pdbx_diffrn_merged_cell.data_section_id (key)


      The value of data_section_id uniquely identifies a data section.



## Category pdbx_diffrn_merged_refln


               Data items in the pdbx_diffrn_merged_refln category record details about the
               merged reflection data set.

---


```
     
         loop_
         _pdbx_diffrn_merged_refln.reflection_id
         _pdbx_diffrn_merged_refln.index_h
         _pdbx_diffrn_merged_refln.index_k
         _pdbx_diffrn_merged_refln.index_l
         _pdbx_diffrn_merged_refln.F_meas_au
         _pdbx_diffrn_merged_refln.F_meas_sigma_au
         _pdbx_diffrn_merged_refln.F_calc_au
         _pdbx_diffrn_merged_refln.phase_calc
         _pdbx_diffrn_merged_refln.status
         _pdbx_diffrn_merged_refln.R_free_flag
         1    0    0    8  918.100   7.0000  2128.50   0.0000 o  1
         2    0    0   10  450.700   5.3000  787.600  180.000 o  1
         3    0    0   12  875.000   7.1000  851.000  180.000 o  10
         4    0    0   14  628.700   6.4000  468.400  180.000 o  10
         5    0    0   18  492.000   7.3000  565.200  180.000 o  5
         # ...
```


---

| Attribute | Key | Required | Type | Units | Enumerated | Bounded |
| --------- | --- | -------- | ---- | ----- | ---------- | ------- |
| DELFWT | no | no | float | None | no | no |
| DELPHWT | no | no | float | None | no | no |
| fom | no | no | float | None | no | yes |
| FWT | no | no | float | None | no | no |
| F_calc_au | no | no | float | arbitrary | no | no |
| F_meas_au | no | no | float | arbitrary | no | no |
| F_meas_sigma_au | no | no | float | arbitrary | no | no |
| index_h | no | yes | int | None | no | no |
| index_k | no | yes | int | None | no | no |
| index_l | no | yes | int | None | no | no |
| intensity_calc | no | no | float | None | no | no |
| intensity_meas | no | no | float | None | no | no |
| intensity_sigma | no | no | float | None | no | no |
| phase_calc | no | no | float | degrees | no | no |
| phase_meas | no | no | float | degrees | no | no |
| PHWT | no | no | float | None | no | no |
| reflection_id | yes | yes | int | None | no | no |
| R_free_flag | no | no | int | None | no | no |
| status | no | no | ucode | None | yes | no |

---

#### _pdbx_diffrn_merged_refln.DELFWT


   The weighted structure factor amplitude for the mFo-DFc map.



#### _pdbx_diffrn_merged_refln.DELPHWT


   The weighted phase for the mFo-DFc map.



#### _pdbx_diffrn_merged_refln.fom


               The figure of merit m for this reflection.



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0.0 | <h3>+&infin;</h3> |


#### _pdbx_diffrn_merged_refln.FWT


   The weighted structure factor amplitude for the 2mFo-DFc map.



#### _pdbx_diffrn_merged_refln.F_calc_au


               The calculated value of the structure factor in arbitrary units.



#### _pdbx_diffrn_merged_refln.F_meas_au


               The measured value of the structure factor after merging in arbitrary units.



#### _pdbx_diffrn_merged_refln.F_meas_sigma_au


               The standard uncertainty (estimated standard deviation) of
                _pdbx_diffrn_merged_refln.F_meas in arbitrary units.



#### _pdbx_diffrn_merged_refln.index_h (required)


               Miller index h of the reflection. The values of the Miller
               indices in this category must correspond to the cell
               defined by cell lengths and cell angles in the pdbx_diffrn_merged_cell category.



#### _pdbx_diffrn_merged_refln.index_k (required)


               Miller index k of the reflection. The values of the Miller
               indices in this category must correspond to the cell
               defined by cell lengths and cell angles in the pdbx_diffrn_merged_cell category.



#### _pdbx_diffrn_merged_refln.index_l (required)


               Miller index l of the reflection. The values of the Miller
               indices in this category must correspond to the cell
               defined by cell lengths and cell angles in the pdbx_diffrn_merged_cell category.



#### _pdbx_diffrn_merged_refln.intensity_calc


               The calculated value of the intensity in the same units as
               _pdbx_diffrn_merged_refln.intensity_meas.



#### _pdbx_diffrn_merged_refln.intensity_meas


               The measured value of the intensity.



#### _pdbx_diffrn_merged_refln.intensity_sigma


               The standard uncertainty (derived from measurement) of the
               intensity in the same units as _pdbx_diffrn_merged_refln.intensity_meas.



#### _pdbx_diffrn_merged_refln.phase_calc


               The calculated structure-factor phase in degrees.



#### _pdbx_diffrn_merged_refln.phase_meas


               The measured structure-factor phase in degrees.



#### _pdbx_diffrn_merged_refln.PHWT


   The weighted phase for the 2mFo-DFc map.



#### _pdbx_diffrn_merged_refln.reflection_id (key)


            A unique identifier for each reflection.



#### _pdbx_diffrn_merged_refln.R_free_flag


               The R-free flag originally assigned to the reflection.  The convention used for
               labeling the work and test sets differs depending on choice of data processing
               software and refinement program.



#### _pdbx_diffrn_merged_refln.status


               Classification of a reflection so as to indicate its status with
               respect to inclusion in the refinement and the calculation of
               R factors.

               The current flags definitions are included but these should
               be reviewed and/or updated as required.



---

| Allowed Values | Detail |
| -------------- | ------ |
| - | systematically absent reflection |
| < |                                      satisfies _refine.ls_d_res_high,
                                      satisfies _refine.ls_d_res_low,
                                      unobserved by _reflns.observed_criterion,
                                      not flagged as systematically absent,
                                      not flagged as unreliable |
| f |                                      satisfies _refine.ls_d_res_high,
                                      satisfies _refine.ls_d_res_low,
                                      observed by _reflns.observed_criterion,
                                      not flagged as systematically absent,
                                      not flagged as unreliable,
                                      excluded from refinement so as to be
                                      included in the calculation of a 'free' R
                                      factor |
| h | does not satisfy _refine.ls_d_res_high |
| l | does not satisfy _refine.ls_d_res_low |
| o |                                      satisfies _refine.ls_d_res_high,
                                      satisfies _refine.ls_d_res_low,
                                      observed by _reflns.observed_criterion,
                                      not flagged as systematically absent,
                                      not flagged as unreliable |
| x | unreliable measurement -- not used |


## Category pdbx_diffrn_merge_crystal_list


              The pdbx_diffrn_merge_crystal_list category lists the identities
              of the crystal samples on which diffraction measurements were
              obtained to make this merged data set.


---


```
     
         loop_
         _pdbx_diffrn_merge_crystal_list.data_section_id
         _pdbx_diffrn_merge_crystal_list.crystal_id
         'ds-unmerged-1'  1
         'ds-unmerged-2'  1
```


---

| Attribute | Key | Required | Type | Units | Enumerated | Bounded |
| --------- | --- | -------- | ---- | ----- | ---------- | ------- |
| crystal_id | yes | yes | int | None | no | no |
| data_section_id | yes | yes | code | None | no | no |

---

#### _pdbx_diffrn_merge_crystal_list.crystal_id (key)


      The value of crystal_id uniquely identifies a crystal sample within a data section.



#### _pdbx_diffrn_merge_crystal_list.data_section_id (key)


      The value of data_section_id uniquely identifies a data section.



## Category pdbx_diffrn_merge_image_list


              The pdbx_diffrn_merge_image_list category lists the image locations
              (spots) on each crystal on which diffraction measurements were
              obtained to make this merged data set.


---


```
     
         loop_
         _pdbx_diffrn_merge_image_list.data_section_id
         _pdbx_diffrn_merge_image_list.crystal_id
         _pdbx_diffrn_merge_image_list.image_id
         'ds-unmerged-1'  1  1
         'ds-unmerged-1'  1  2
         'ds-unmerged-2'  1  1
         'ds-unmerged-2'  1  2
     
```


---

| Attribute | Key | Required | Type | Units | Enumerated | Bounded |
| --------- | --- | -------- | ---- | ----- | ---------- | ------- |
| crystal_id | yes | yes | int | None | no | no |
| data_section_id | yes | yes | code | None | no | no |
| image_id | yes | yes | int | None | no | no |

---

#### _pdbx_diffrn_merge_image_list.crystal_id (key)


      The value of crystal_id uniquely identifies a crystal sample within a data section.



#### _pdbx_diffrn_merge_image_list.data_section_id (key)


      The value of data_section_id uniquely identifies a data section.



#### _pdbx_diffrn_merge_image_list.image_id (key)


      The value of image_id uniquely identifies a location (spot) on a crystal sample.



## Category pdbx_diffrn_merge_rejected_list


              The pdbx_diffrn_merge_rejected_list category lists the rejected reflections
              from the image spots from the crystals from the parent data set used to make
              this merged data set.

---


```
     
        loop_
         _pdbx_diffrn_merge_rejected_list.data_section_id
         _pdbx_diffrn_merge_rejected_list.reflection_id
         _pdbx_diffrn_merge_rejected_list.image_id
         'ds-unmerged-1'  1  1
         'ds-unmerged-1'  2  1
         'ds-unmerged-2'  5  1
     
     
```


---

| Attribute | Key | Required | Type | Units | Enumerated | Bounded |
| --------- | --- | -------- | ---- | ----- | ---------- | ------- |
| data_section_id | yes | yes | code | None | no | no |
| image_id | yes | yes | int | None | no | no |
| reflection_id | yes | yes | int | None | no | no |

---

#### _pdbx_diffrn_merge_rejected_list.data_section_id (key)


      The value of data_section_id uniquely identifies a data section.



#### _pdbx_diffrn_merge_rejected_list.image_id (key)


      The value of image_id uniquely identifies a location (spot) on a crystal sample.



#### _pdbx_diffrn_merge_rejected_list.reflection_id (key)


      The value of reflection_id uniquely identifies a reflection in the parent data section.



## Category pdbx_diffrn_merge_stat


               Data items in the pdbx_diffrn_merge_stat category record details about the
               reflection data in this merged data set.

---


```
     
         _pdbx_diffrn_merge_stat.data_section_id               'ds-merge-1'
         _pdbx_diffrn_merge_stat.d_resolution_high              1.32
         _pdbx_diffrn_merge_stat.d_resolution_low               150.0
         _pdbx_diffrn_merge_stat.number_obs                     300000
         _pdbx_diffrn_merge_stat.number_all                     308123
         _pdbx_diffrn_merge_stat.mean_I_over_sigI_all           10.7
         _pdbx_diffrn_merge_stat.Rmerge_all                     0.069
         _pdbx_diffrn_merge_stat.Rpim_I_all                     0.033
         _pdbx_diffrn_merge_stat.CC_half_all                    0.999
         _pdbx_diffrn_merge_stat.percent_possible_obs           98.2
```


---

| Attribute | Key | Required | Type | Units | Enumerated | Bounded |
| --------- | --- | -------- | ---- | ----- | ---------- | ------- |
| CC_half_all | no | no | float | None | no | yes |
| data_section_id | yes | yes | code | None | no | no |
| details | no | no | text | None | no | no |
| d_resolution_high | no | no | float | angstroms | no | yes |
| d_resolution_low | no | no | float | angstroms | no | yes |
| mean_I_over_sigI_all | no | no | float | None | no | no |
| number_all | no | no | int | None | no | yes |
| number_obs | no | no | int | None | no | yes |
| observed_criterion_I_max | no | no | float | None | no | no |
| observed_criterion_I_min | no | no | float | None | no | no |
| observed_criterion_sigma_I | no | no | float | None | no | no |
| percent_possible_obs | no | no | float | None | no | yes |
| Rmerge_all | no | no | float | None | no | yes |
| Rpim_I_all | no | no | float | None | no | yes |

---

#### _pdbx_diffrn_merge_stat.CC_half_all


              The Pearson's correlation coefficient expressed as a decimal value
              between the average intensities from randomly selected
              half-datasets.

          Ref: Karplus & Diederichs (2012), Science 336, 1030-33



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| -1.0 | 1.0 |


#### _pdbx_diffrn_merge_stat.data_section_id (key)


      The value of data_section_id uniquely identifies a data section.



#### _pdbx_diffrn_merge_stat.details


               A description of reflection data not covered by other data
               names.



#### _pdbx_diffrn_merge_stat.d_resolution_high


               The smallest value for the interplanar spacings for
               the reflection data. This is called the highest resolution.



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0.0 | <h3>+&infin;</h3> |


#### _pdbx_diffrn_merge_stat.d_resolution_low


               The largest value for the interplanar spacings for the
               reflection data. This is called the lowest resolution.



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0.0 | <h3>+&infin;</h3> |


#### _pdbx_diffrn_merge_stat.mean_I_over_sigI_all


               The mean of the ratio of the intensities of all reflections
               in this shell to the mean of the standard uncertainties of the
               intensities of all reflections.



#### _pdbx_diffrn_merge_stat.number_all


               The total number of reflections contributing to this data set.



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0 | <h3>+&infin;</h3> |


#### _pdbx_diffrn_merge_stat.number_obs


               The number of reflections satisfying the observed criteria.



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0 | <h3>+&infin;</h3> |


#### _pdbx_diffrn_merge_stat.observed_criterion_I_max


               The criterion used to classify a reflection as 'observed'
               expressed as an upper limit for the value of I.



#### _pdbx_diffrn_merge_stat.observed_criterion_I_min


               The criterion used to classify a reflection as 'observed'
               expressed as a lower limit for the value of I.



#### _pdbx_diffrn_merge_stat.observed_criterion_sigma_I


               The criterion used to classify a reflection as 'observed'
               expressed as a multiple of the value of sigma(I).



#### _pdbx_diffrn_merge_stat.percent_possible_obs


               The percentage of geometrically possible reflections that satisfy
               the resolution limits established by _pdbx_diffrn_merge_stat.d_resolution_high and _pdbx_diffrn_merge_stat.d_resolution_low and the observation limit established
                in creating this data set.



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0.0 | 100.0 |


#### _pdbx_diffrn_merge_stat.Rmerge_all


               Residual factor Rmerge for all reflections that satisfy the
               resolution limits established by _pdbx_diffrn_merge_stat.d_resolution_high
               and _pdbx_diffrn_merge_stat.d_resolution_low.




---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0.0 | <h3>+&infin;</h3> |


#### _pdbx_diffrn_merge_stat.Rpim_I_all


              The precision-indicating merging R factor value Rpim,
              for merging all intensities in this data set.

              Ref: Diederichs, K. & Karplus, P. A. (1997). Nature Struct.
                   Biol. 4, 269-275.
                   Weiss, M. S. & Hilgenfeld, R. (1997). J. Appl. Cryst.
                   30, 203-205.
                   Weiss, M. S. (2001). J. Appl. Cryst. 34, 130-135.



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0.0 | <h3>+&infin;</h3> |


## Category pdbx_diffrn_merge_stat_shell


               Data items in the pdbx_diffrn_merge_stat_shell category record details about the
               reflection data in resolution shells in this merged data set.

---


```
     
         _pdbx_diffrn_merge_stat_shell.ordinal_id                        1
         _pdbx_diffrn_merge_stat_shell.d_resolution_high              1.32
         _pdbx_diffrn_merge_stat_shell.d_resolution_low               1.60
         _pdbx_diffrn_merge_stat_shell.number_obs                     1500
         _pdbx_diffrn_merge_stat_shell.number_all                     1530
         _pdbx_diffrn_merge_stat_shell.mean_I_over_sigI_all           10.7
         _pdbx_diffrn_merge_stat_shell.Rmerge_all                     0.072
         _pdbx_diffrn_merge_stat_shell.Rpim_I_all                     0.037
         _pdbx_diffrn_merge_stat_shell.CC_half_all                    0.980
         _pdbx_diffrn_merge_stat_shell.percent_possible_obs           98.0
```


---

| Attribute | Key | Required | Type | Units | Enumerated | Bounded |
| --------- | --- | -------- | ---- | ----- | ---------- | ------- |
| CC_half_all | no | no | float | None | no | yes |
| d_resolution_high | no | yes | float | angstroms | no | yes |
| d_resolution_low | no | yes | float | angstroms | no | yes |
| mean_I_over_sigI_all | no | no | float | None | no | no |
| number_all | no | no | int | None | no | yes |
| number_obs | no | no | int | None | no | yes |
| observed_criterion_I_max | no | no | float | None | no | no |
| observed_criterion_I_min | no | no | float | None | no | no |
| observed_criterion_sigma_I | no | no | float | None | no | no |
| ordinal_id | yes | yes | code | None | no | no |
| percent_possible_obs | no | no | float | None | no | yes |
| Rmerge_all | no | no | float | None | no | yes |
| Rpim_I_all | no | no | float | None | no | yes |

---

#### _pdbx_diffrn_merge_stat_shell.CC_half_all


              The Pearson's correlation coefficient expressed as a decimal value
              between the average intensities from randomly selected
              half-sets in this resolution shell.

          Ref: Karplus & Diederichs (2012), Science 336, 1030-33



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| -1.0 | 1.0 |


#### _pdbx_diffrn_merge_stat_shell.d_resolution_high (required)


               The smallest value for the interplanar spacings for
               the reflection data in the shell.



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0.0 | <h3>+&infin;</h3> |


#### _pdbx_diffrn_merge_stat_shell.d_resolution_low (required)


               The largest value for the interplanar spacings for the
               reflection data in the shell.



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0.0 | <h3>+&infin;</h3> |


#### _pdbx_diffrn_merge_stat_shell.mean_I_over_sigI_all


               The mean of the ratio of the intensities of all reflections
               in this shell to the mean of the standard uncertainties of the
               intensities of reflections in this resoution shell.



#### _pdbx_diffrn_merge_stat_shell.number_all


               The total number of reflections contributing to this resolution shell.



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0 | <h3>+&infin;</h3> |


#### _pdbx_diffrn_merge_stat_shell.number_obs


               The number of reflections satisfying the observed criteria.



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0 | <h3>+&infin;</h3> |


#### _pdbx_diffrn_merge_stat_shell.observed_criterion_I_max


               The criterion used to classify a reflection as 'observed'
               expressed as an upper limit for the value of I.



#### _pdbx_diffrn_merge_stat_shell.observed_criterion_I_min


               The criterion used to classify a reflection as 'observed'
               expressed as a lower limit for the value of I.



#### _pdbx_diffrn_merge_stat_shell.observed_criterion_sigma_I


               The criterion used to classify a reflection as 'observed'
               expressed as a multiple of the value of sigma(I).



#### _pdbx_diffrn_merge_stat_shell.ordinal_id (key)


      The value of ordinal_id uniquely identifies a resolution shell.



#### _pdbx_diffrn_merge_stat_shell.percent_possible_obs


               The percentage of geometrically possible reflections that satisfy
               the resolution limits established by _pdbx_diffrn_merge_stat_shell.d_resolution_high and _pdbx_diffrn_merge_stat_shell.d_resolution_low and the observation limit established
                for this resolution shell.



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0.0 | 100.0 |


#### _pdbx_diffrn_merge_stat_shell.Rmerge_all


               Residual factor Rmerge for all reflections that satisfy the
               resolution limits established by _pdbx_diffrn_merge_stat_shell.d_resolution_high
               and _pdbx_diffrn_merge_stat_shell.d_resolution_low.




---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0.0 | <h3>+&infin;</h3> |


#### _pdbx_diffrn_merge_stat_shell.Rpim_I_all


              The precision-indicating merging R factor value Rpim,
              for merging all intensities in this resoution shell.

              Ref: Diederichs, K. & Karplus, P. A. (1997). Nature Struct.
                   Biol. 4, 269-275.
                   Weiss, M. S. & Hilgenfeld, R. (1997). J. Appl. Cryst.
                   30, 203-205.
                   Weiss, M. S. (2001). J. Appl. Cryst. 34, 130-135.



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0.0 | <h3>+&infin;</h3> |


## Category pdbx_diffrn_merge_wavelength_list


               Data items in the pdbx_diffrn_merge_wavelength_list category
               record the wavelength(s) of the radiation used to measure the
               diffraction intensities in this merged data set.

---


```
     
     #
      loop_
      _pdbx_diffrn_merge_wavelength_list.id
      _pdbx_diffrn_merge_wavelength_list.wavelength
      1  0.91837
```


---

| Attribute | Key | Required | Type | Units | Enumerated | Bounded |
| --------- | --- | -------- | ---- | ----- | ---------- | ------- |
| id | yes | yes | int | None | no | no |
| wavelength | no | yes | float | angstroms | no | yes |

---

#### _pdbx_diffrn_merge_wavelength_list.id (key)


        The code identifying each value of _pdbx_diffrn_merge_wavelength_list.wavelength.



#### _pdbx_diffrn_merge_wavelength_list.wavelength (required)


               The radiation wavelength in angstroms.



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0.0 | <h3>+&infin;</h3> |


## Category pdbx_diffrn_symmetry


               Data items in the category record details about the space-group symmetry.

---


```
     
     _pdbx_diffrn_symmetry.data_section_id        'ds-merged-1'
     _pdbx_diffrn_symmetry.space_group_name_H-M   'P 21 21 21'
     #
```


---

| Attribute | Key | Required | Type | Units | Enumerated | Bounded |
| --------- | --- | -------- | ---- | ----- | ---------- | ------- |
| data_section_id | yes | yes | code | None | no | no |
| space_group_name_H-M | no | yes | line | None | no | no |

---

#### _pdbx_diffrn_symmetry.data_section_id (key)


      The value of data_section_id uniquely identifies a data section.



#### _pdbx_diffrn_symmetry.space_group_name_H-M (required)


               Hermann-Mauguin space-group symbol.



## Category pdbx_diffrn_unmerged_cell


               Data items in the pdbx_diffrn_unmerged_cell category record details about the
               crystallographic cell parameters for this unmerged data set

---


```
     
         #
         loop_
         _pdbx_diffrn_unmerged_cell.ordinal
         _pdbx_diffrn_unmerged_cell.crystal_id
         _pdbx_diffrn_unmerged_cell.wavelength
         _pdbx_diffrn_unmerged_cell.cell_length_a
         _pdbx_diffrn_unmerged_cell.cell_length_b
         _pdbx_diffrn_unmerged_cell.cell_length_c
         _pdbx_diffrn_unmerged_cell.cell_angle_alpha
         _pdbx_diffrn_unmerged_cell.cell_angle_beta
         _pdbx_diffrn_unmerged_cell.cell_angle_gamma
         1 1 .91837  51.3940 109.0130 137.3070 90.000 90.000 90.000
         2 2 .91837  51.3940 109.0130 137.3070 90.000 90.000 90.000
         # ...  abbreviated ...
```


---

| Attribute | Key | Required | Type | Units | Enumerated | Bounded |
| --------- | --- | -------- | ---- | ----- | ---------- | ------- |
| cell_angle_alpha | no | no | float | degrees | no | yes |
| cell_angle_beta | no | no | float | degrees | no | yes |
| cell_angle_gamma | no | no | float | degrees | no | yes |
| cell_length_a | no | no | float | angstroms | no | yes |
| cell_length_b | no | no | float | angstroms | no | yes |
| cell_length_c | no | no | float | angstroms | no | yes |
| cell_volume | no | no | float | angstroms_cubed | no | yes |
| crystal_id | no | yes | int | None | no | no |
| ordinal | yes | yes | int | None | no | no |
| wavelength | no | yes | float | angstroms | no | yes |

---

#### _pdbx_diffrn_unmerged_cell.cell_angle_alpha


               Unit-cell angle alpha in degrees.



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0.0 | 180.0 |


#### _pdbx_diffrn_unmerged_cell.cell_angle_beta


               Unit-cell angle beta in degrees.



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0.0 | 180.0 |


#### _pdbx_diffrn_unmerged_cell.cell_angle_gamma


               Unit-cell angle gamma in degrees.



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0.0 | 180.0 |


#### _pdbx_diffrn_unmerged_cell.cell_length_a


               Unit-cell length a in angstroms.



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0.0 | <h3>+&infin;</h3> |


#### _pdbx_diffrn_unmerged_cell.cell_length_b


               Unit-cell length b reported in angstroms.



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0.0 | <h3>+&infin;</h3> |


#### _pdbx_diffrn_unmerged_cell.cell_length_c


               Unit-cell length c reported in angstroms.



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0.0 | <h3>+&infin;</h3> |


#### _pdbx_diffrn_unmerged_cell.cell_volume


               Cell volume V in angstroms cubed.

               V = a b c (1 - cos^2^~alpha~ - cos^2^~beta~ - cos^2^~gamma~
                          + 2 cos~alpha~ cos~beta~ cos~gamma~)^1/2^

               a     = _pdbx_diffrn_unmerged_cell.cell_length_a
               b     = _pdbx_diffrn_unmerged_cell.cell_length_b
               c     = _pdbx_diffrn_unmerged_cell.cell_length_c
               alpha = _pdbx_diffrn_unmerged_cell.cell_angle_alpha
               beta  = _pdbx_diffrn_unmerged_cell.cell_angle_beta
               gamma = _pdbx_diffrn_unmerged_cell.cell_angle_gamma



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0.0 | <h3>+&infin;</h3> |


#### _pdbx_diffrn_unmerged_cell.crystal_id (required)


      The value of crystal_id uniquely identifies a crystal sample within a data section.



#### _pdbx_diffrn_unmerged_cell.ordinal (key)


      Ordinal index for the admin section.



#### _pdbx_diffrn_unmerged_cell.wavelength (required)


               The radiation wavelength in angstroms.



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0.0 | <h3>+&infin;</h3> |


## Category pdbx_diffrn_unmerged_refln


               Data items in the pdbx_diffrn_unmerged_refln category record details about an
               unmerged reflection data set.

---


```
     
         #
          loop_
         _pdbx_diffrn_unmerged_refln.reflection_id
         _pdbx_diffrn_unmerged_refln.image_id_begin
         _pdbx_diffrn_unmerged_refln.image_id_end
         _pdbx_diffrn_unmerged_refln.index_h
         _pdbx_diffrn_unmerged_refln.index_k
         _pdbx_diffrn_unmerged_refln.index_l
         _pdbx_diffrn_unmerged_refln.intensity_meas
         _pdbx_diffrn_unmerged_refln.intensity_sigma
         _pdbx_diffrn_unmerged_refln.phi_reflection
         1  1  1    0    0    5     28.800  264.700  .500
         # ... abbreviated ...
```


---

| Attribute | Key | Required | Type | Units | Enumerated | Bounded |
| --------- | --- | -------- | ---- | ----- | ---------- | ------- |
| image_id_begin | no | yes | int | None | no | no |
| image_id_end | no | yes | int | None | no | no |
| index_h | no | yes | int | None | no | no |
| index_k | no | yes | int | None | no | no |
| index_l | no | yes | int | None | no | no |
| intensity_meas | no | no | float | None | no | no |
| intensity_profile | no | no | float | None | no | no |
| intensity_profile_sigma | no | no | float | None | no | no |
| intensity_sigma | no | no | float | None | no | no |
| intensity_sum | no | no | float | None | no | no |
| intensity_sum_sigma | no | no | float | None | no | no |
| partiality | no | no | float | None | no | yes |
| phi_reflection | no | no | float | None | no | no |
| reflection_id | yes | yes | int | None | no | no |

---

#### _pdbx_diffrn_unmerged_refln.image_id_begin (required)


      The initial value of a range of image_id values.



#### _pdbx_diffrn_unmerged_refln.image_id_end (required)


      The terminal value of a range of image_id values.



#### _pdbx_diffrn_unmerged_refln.index_h (required)


               Miller index h of the reflection. The values of the Miller
               indices in this category must correspond to the cell
               defined by cell lengths and cell angles in the pdbx_diffrn_unmerged_cell category.



#### _pdbx_diffrn_unmerged_refln.index_k (required)


               Miller index k of the reflection. The values of the Miller
               indices in this category must correspond to the cell
               defined by cell lengths and cell angles in the pdbx_diffrn_unmerged_cell category.



#### _pdbx_diffrn_unmerged_refln.index_l (required)


               Miller index l of the reflection. The values of the Miller
               indices in this category must correspond to the cell
               defined by cell lengths and cell angles in the pdbx_diffrn_unmerged_cell category.



#### _pdbx_diffrn_unmerged_refln.intensity_meas


               The measured value of the intensity.



#### _pdbx_diffrn_unmerged_refln.intensity_profile


               The intensity obtained from profile.



#### _pdbx_diffrn_unmerged_refln.intensity_profile_sigma


               The standard uncertainty (derived from profile) of the
               intensity in the same units as _pdbx_diffrn_unmerged_refln.intensity_profile.



#### _pdbx_diffrn_unmerged_refln.intensity_sigma


               The standard uncertainty (derived from measurement) of the
               intensity in the same units as _pdbx_diffrn_unmerged_refln.intensity_meas.



#### _pdbx_diffrn_unmerged_refln.intensity_sum


               The intensity obtained from summation.



#### _pdbx_diffrn_unmerged_refln.intensity_sum_sigma


               The standard uncertainty (derived from summation) of the
               intensity in the same units as _pdbx_diffrn_unmerged_refln.intensity_sum.



#### _pdbx_diffrn_unmerged_refln.partiality


               The partiality value for the reflection.



---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 0.0 | 1.0 |


#### _pdbx_diffrn_unmerged_refln.phi_reflection


               The phi value for the reflection.



#### _pdbx_diffrn_unmerged_refln.reflection_id (key)


            A unique identifier for each reflection.


