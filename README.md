# munin-plugin-condor

Various munin plugins for condor

To install, git clone this project and create symlink in /etc/munin/plugins to various plugin scripts (like condor_schedd) inside the git root directory. 

## condor_schedd

Monitors number of jobs running, idle, etc.. (just looks at /var/lib/condor-cron/spool/.schedd_classad)

By default, it monitors /var/lib/condor/spool/.schedd_classad and a few attrbitues. Create a config file inside /etc/munin/plugin-conf.d to configre.

[/etc/munin/plugin-conf.d/munin-plugin-condor]
```
[condor_schedd]
env.classad_path=/var/lib/condor/spool/.schedd_classad
env.classad_attrs=TotalLocalJobsRunning,TotalLocalJobsIdle
```

For a list of attribute you can monitor, just look at your .schedd_classad file.


