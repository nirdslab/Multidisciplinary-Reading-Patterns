# Multidisciplinary Reading Patterns of Digital Documents

Multidisciplinary Reading Patterns is an eye-tracking dataset consisting of reading patterns of researchers on scientific literature.
In the initial version, we include reading patterns of seven doctoral students on two articles collected using a [PupilLabs Core](https://pupil-labs.com/products/core/) eye tracker.
The repository includes both raw data (excluding PupilLabs generated files, including manual annotations), and processed data.

## Dataset

### Raw Data
Raw pupillary, fixation data after processing annotations are included in the `dataset/raw` folder in the format
`<participant-number>-<article>-<dataset-type>.csv`.

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
Dataset after being processed using [Real-Time Advanced Eye Movements Analysis Pipeline (RAEMAP)](https://doi.org/10.1145/3379157.3391992) is included in `dataset/processed` folder, with (1) Gaze data and (2) Pupil data.

#### File Content


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

## Contact
* Twitter: [@NirdsLab](https://twitter.com/NirdsLab/)
* Web: [https://nirdslab.github.io/](https://nirdslab.github.io/)

## License
[CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)
