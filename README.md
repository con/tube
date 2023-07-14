# CONTube

DataLad dataset to collect various videos produced at CON.

# Instructions

## Metadata

Some might not be yet in shareable state -- git-anex metadata will be used to annotate versions of the files as they could not be distributed.
E.g. in this case, while setting "venue" metadata field `git-annex` shows that files already have set `distribution-restrictions=uncurated` and so we would not redistribute those publicly.

## Editing

Videos should be curated and edited before made public.

A coarse list of steps:

- (once) `datalad clone secretserver:/mnt/btrfs/datasets/con/tube`
- `datalad get file.mp4`
- `git annex unlock file.mp4`
- Use open source tools such as OBS, openshot etc TODO: basic instructions
- `datalad save -m "Description" file.mp4`
- if ready for redistribution - `git annex metadata -r "distribution-restrictions" file.mp4`
- `datalad push --to=origin`

