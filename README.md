# Multidisciplinary Reading Patterns of Digital Documents

Multidisciplinary Reading Patterns is an eye-tracking dataset consisting of reading patterns of researchers on scientific literature.
In the initial version, we include reading patterns of seven doctoral students on two articles collected using a [PupilLabs Core](https://pupil-labs.com/products/core/) eye tracker.
The repository includes both raw data and processed data.

## Dataset

### Raw Data
Raw pupillary, fixation data after processing annotations are included in the [`dataset/raw`](dataset/raw) folder in the format
`<participant-number>-<article>-<dataset-type>.csv`.
**Note:** Raw data does not include files generated by PupilLabs export tools.

| Property              |Description                                         |
|---                    |---                                                                            |
|`participant-number`   | P01 - P07                                                                          |
|`article`              | `WDILL` - Computer Science article, `PHY` - Physics article                   |
|`dataset-type`         | `gaze` - Gaze data, `pupil` - Pupillometric data, `combined` - Pupil + Gaze   |

#### File Content

| Property  | Description |
|---        |---          |
|`gaze_timestamp`, `pupil_timestamp` | Timestamp of source image frame (generated from PupilLabs)|
|`world_index`    | World video (from outward facing camera) frame index      |
|`confidence`     | Confidence of gaze/ pupil estimates (0 - not confident, 1 - confident) |
|`norm_pos_x`,`norm_pos_y` | Normalized gaze position on screen |
|`label`          | Manual annotation for section of the paper |
|`diameter`       | Diameter of pupil dilation  |
|`order`          | Sequence number to indicate order of visit |


### Processed Data
Dataset after being processed using [Real-Time Advanced Eye Movements Analysis Pipeline (RAEMAP)](https://doi.org/10.1145/3379157.3391992) is included in [`dataset/processed`](dataset/processed) folder, with (1) Gaze data and (2) Pupil data.

#### Gaze Data Content

| Property            | Description |
|---                  |---          |
|`fxtn_count`         | Fixation count            |
|`avg_fxtn_duration`  | Average fixation duration |
|`total_fxtn_dur`     | Total fixation duration   |
|`std_fxtn_dur`| |
|`total_sacc_dur`| |
|`avg_sacc_dur`| |
|`max_sacc_amplitude`| |
|`min_sacc_amplitude`| |
|`avg_sacc_amplitude`| |
|`std_sacc_amplitude`| |

#### Pupil Data Content

|Property       | Desctiption   |
|---            |---            |
|`LHIPA`|[The Low/High Index of Pupillary Activity](https://doi.org/10.1145/3313831.3376394) |
|`pavg`| |
|`pcpd`| |



## Cite
If you're using this dataset in your research, please cite following publication.
```
@inproceedings{10.1145/3517031.3531630,
  author = {Mahanama, Bhanuka and Jayawardena, Gavindya and and Abeysinghe, Yasasi and Ashok, Vika and Jayarathna, Sampath},
  title = {Multidisciplinary Reading Patterns of Digital Documents},
  year = {2022},
  isbn = {978-1-4503-9252-5/22/06},
  publisher = {Association for Computing Machinery},
  address = {New York, NY, USA},
  url = {https://doi.org/10.1145/3517031.3531630},
  doi = {10.1145/3517031.3531630},
  booktitle = {Proceedings of the 2022 Symposium on Eye Tracking Research and Applications},
  location = {Seattle, WA, USA},
  series = {ETRA '22}
}
```

### Similar Studies
1. **[Analyzing the Effect of Reading Patterns using Eye Tracking Measures](https://doi.org/10.1145/3383583.3398591)**
```
@inproceedings{10.1145/3383583.3398591,
  author = {Jayawardena, Gavindya and Jayarathna, Sampath and Wu, Jian},
  title = {Analyzing the Effect of Reading Patterns Using Eye Tracking Measures},
  year = {2020},
  isbn = {9781450375856},
  publisher = {Association for Computing Machinery},
  address = {New York, NY, USA},
  url = {https://doi.org/10.1145/3383583.3398591},
  booktitle = {Proceedings of the ACM/IEEE Joint Conference on Digital Libraries in 2020},
  pages = {517???518}
}
```

2. **[Analyzing Unconstrained Reading Patterns of Digital Documents Using Eye Tracking](https://doi.org/10.1109/JCDL52503.2021.00036)**

```
@INPROCEEDINGS{10.1109/JCDL52503.2021.00036,
  author={Mahanama, Bhanuka and Jayawardena, Gavindya and Jayarathna, Sampath},
  booktitle={2021 ACM/IEEE Joint Conference on Digital Libraries (JCDL)},
  title={Analyzing Unconstrained Reading Patterns of Digital Documents Using Eye Tracking},
  year={2021},
  pages={282-283},
  doi={10.1109/JCDL52503.2021.00036},
  organization={IEEE}
}

```


## Contact
* Twitter: [@NirdsLab](https://twitter.com/NirdsLab/)
* Web: [https://nirdslab.github.io/](https://nirdslab.github.io/)

## License
[CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)
