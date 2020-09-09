# Example Databases

This is an example database set written for the [AVHD-AS / P.NATS Phase 2 Processing Chain](https://github.com/pnats2avhd/processing-chain).

## Types of Databases

During the ITU-T/VQEG project, the databases were assigned as "Long" or "Short". Short databases used conditions which were homogenous during the whole video, only one resolution and bitrate per video clip of 8-10 s. Long database conditions could contain multiple bitrates and resolutions in an adaptive pattern and also stalling events.

The supplied test specification `.yaml`-files correspond to one of each of these Long and Short test databases.

## Database YAML

Each database is mainly specified by a `.yaml` file that lists:

- The source files used for encoding
- The settings for encoding audio and video
- The HRC settings for "stitching" together different encodings

Some general definitions:

- A database is a collection of PVSes (Processed Video Sequences)
- A PVS is a combination of SRC and HRC (Hypothetical Reference Circuit)
- PVS, SRC and HRC IDs must be unique over all databases (SRC/HRC IDs can be identified across databases)
- A PVS file processed for being read by a pixel-based model is called AVPVS
- A PVS file shown in a particular context is a CPVS (Context Processed Video Sequence)

Each database (short and long) must reside in its own folder, where the folder name is equal to the database ID.

See the example YAML files in the respective subfolders.

## Utilities

This repository also contains tools for creating and analysing database specifications.

## Authors

- David Lindero, Ericsson – <david.lindero@ericsson.com>

## License

Copyright (c) 2020, P.NATS Phase 2 / AVHD-AS Developers.

Licensed under GNU General Public License v3, see `LICENSE.md`.

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.
