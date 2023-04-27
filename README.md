# NeSI CESM config

To install these files copy them to *~/.cime/* and replace *nesi99999* with
your NeSI project code, for example run the following (where *nesi12345* is your project code):

```sh
mkdir -p ~/.cime
sed 's/nesi99999/nesi12345/g' config_machines.xml > ~/.cime/config_machines.xml
cp config_batch.xml ~/.cime/config_batch.xml
```
### Troubleshoooting

If you encounter `"err=Can't locate XML/LibXML.pm in @INC (you may need to install the XML::LibXML module)"`, install the missing perl dependency with following two commands

```
curl -L [https://cpanmin.us](https://cpanmin.us/) | perl - App::cpanminus 
cpanm XML::LibXML
```

and then export installation path with `export PERL5LIB=~/perl5/lib/perl5/x86_64-linux-thread-multi`  (OR you can add that export .. command to your *~/.bashrc* file)