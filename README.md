# NeSI CESM config

To install these files copy them to *~/.cime/* and replace *nesi99999* with
your NeSI project code, for example run the following:

```sh
mkdir -p ~/.cime
sed 's/nesi99999/nesi12345/g' config_machines.xml > ~/.cime/config_machines.xml
cp config_batch.xml ~/.cime/config_batch.xml
```
