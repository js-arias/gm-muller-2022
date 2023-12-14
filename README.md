# Muller et al. 2022 Model

This model is imported from the optimized plate rotation model
of Müller et al. (2022)
that can downloaded from the [EarthByte page](https://earthbyte.org/webdav/ftp/Data_Collections/Muller_etal_2022_SE/).

## Time frame

The rotations are defined from 540 million years age
(up to 600 to the plate motion model)
to today,
in time stages of 5 million years.

## Pixelation

The model is available in three resolutions:
e360 (360 pixels in the equatorial ring),
e180,
and e120.
For reference,
Pixel IDs are stored as `pixel-ids-xxx.tab`,
in which `xxx` is used to indicate the resolution.

## File description

All the files are prefixed as `muller-*`
usually followed by the pixelation resolution,
the size of the time step,
and the kind of file.

### Pixelated features

It is based on the continent polygons
from Merdith et al. (2021),
extended with the volcanic provinces from Johansson et al. (2018).
It is stored in the file `muller-pixels-xxx.tab`
in which `xxx` is used to indicate the resolution.

### Plate motion model

The plate motion model
(or rotation model)
was based on the tectonic rule optimized rotation model
of Müller et al. (2022).

The model is stored in the file `muller-motion-xxx-5.tab`,
in which `xxx` is the pixel resolution,
and 5 is the time resolution (in million years).

### Paleolandscape

The paleolandscape model from 0-400 Ma was constructed by taken
the [unrotated model of Cao et al. (2017)](https://github.com/js-arias/gml-cao)
and then rotating the pixels using the Muller et al. (2022) rotation.
For the 405-540 Ma time frame,
it use the [unrotated PaleoMap model of Scotese and Wright (2018)](https://github.com/js-arias/gml-paleomap).
Layers at present time are derived
from [NaturalEarth](https://www.naturalearthdata.com/)
and [NaturalEarth III](https://www.shadedrelief.com/natural3/index.html).

As the paleolandscape is derived from unrotated models,
it will have some gaps for landscapes features in the original models
that can not be associated with a moving plate
(for example the mountain ranges between India and Asia,
just before the India collision).

The landscape model uses the following convention:

Key | Environment
--- | -----------
  1 | oceanic plateaus
  2 | continental shelf
  3 | lowlands
  4 | highlands
  5 | ice sheets

The model is stored in the file `muller-landscape-cao-paleomap-xxx-5.tab`,

in which `xxx` is the pixel resolution,
and 5 is the time resolution (in million years).

A color key,
which is compatible with color-blindness,
and can be used with `plates timepix map` command
is stored in the file `muller-landscape-cao-paleomap-key.tab`.

## Citation and data license

This model is the direct process of the
Cao et al. (2017),
Scotese and Wright (2018),
Merdith et al. (2021),
and Müller et al. (2022) and  models.
As such,
the original publications should be cited when the model is used.
Relevant papers are given in this file
and provided as bibTeX.

It is not required to cite this repository,
but if you do not include the model in the supplementary material
of your publication,
it might be a good idea to link this repository
and help others to replicate or re-use your analysis.

Data from PaleoMap project
(Scotese and Wrigth, 2018)
is distributed under the CC-BY 4.0 license.

## Disclaimer

As the models are a product of a pixelation of vectorial models,
it is possible that some pixels will not be defined
particularly in the boundaries of plates.
Depending on the usage given to the models,
this problems will be only annoying
(for example,
a deep ocean pixel in the middle of a continent),
or it can be critical
(if the feature of interest is near this absent pixels).
So be careful when using the models.

## References

Cao, W. et al.
(2017)
Improving global paleogeography since the late Paleozoic using paleobiology.
Biogeosciences, 14, 5425-5439.
DOI: [10.5194/bg-14-5425-2017](https://doi.org/10.5194/bg-14-5425-2017).

Johansson, L., Zahirovic, S., & Müller, R. D.
(2018).
The interplay between the eruption and weathering of large igneous provinces and the deep‐time carbon cycle.
Geophysical Research Letters, 45, 5380-5389.
DOI: [10.1029/2017GL076691](https://doi.org/10.1029/2017GL076691).

Merdith, A. S. et al.
(2021)
Extending full-plate tectonic models into deep time: Linking the Neoproterozoic and the Phanerozoic.
Earth-Science Reviews, 241, 103477.
DOI: [10.1016/j.earscirev.2020.103477](https://doi.org/10.1016/j.earscirev.2020.103477).

Müller, R. D. et al.
(2022)
A tectonic-rules-based mantle reference frame since 1 billion years ago – implications for supercontinent cycles and plate–mantle system evolution.
Solid Earth, 12, 1127-1159.
DOI: [10.5194/se-13-1127-2022](https://doi.org/10.5194/se-13-1127-2022).

Scotese, C.S., Wrigth, N.
(2018)
PALEOMAP Paleodigital elevation models (PaleoDEMs) for Phanerozoic.
URL: <https://www.earthbyte.org/paleodem-resource-scotese-and-wright-2018/>.
