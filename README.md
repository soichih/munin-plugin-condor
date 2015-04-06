# munin-plugin-condor
various munin plugins for condor

* schedd_classad (/var/lib/condor-cron/spool/.schedd_classad)

Monitors number of jobs running, idle, etc.. 

To install, just git clone this project, and create symlink from /etc/munin/plubins directory. By default, it monitors /var/lib/condor/spool/.schedd_classad and a few attrbitues. Create a config file inside /etc/munin/plugin-conf.d to configre.

[/etc/munin/plugin-conf.d/munin-plugin-condor]
> [condor_schedd]
> env.classad_path=/var/lib/condor/spool/.schedd_classad
> env.classad_attrs=TotalLocalJobsRunning,TotalLocalJobsIdle

For a list of attribute you can monitor, just look at your .schedd_classad file.


