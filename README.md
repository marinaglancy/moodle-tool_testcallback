# Test plugin for https://github.com/lmscloud-io/moodle-tool_vault/compare/newcallback suggestion

What I did:
- backed up a site that does not have a tool_testcallback installed
- restored on a site that has tool_testcallback
- the callback was executed on each stage:


```
[10/10/24, 23:03:22] [info] Restore scheduled
[10/10/24, 23:03:24] [info] [pid 1049915] Preparing to restore
[10/10/24, 23:03:25] [info] [pid 1049915] Downloading file dbstructure.zip ...
[10/10/24, 23:03:25] [info] [pid 1049915] ...done
[10/10/24, 23:03:25] [info] [pid 1049915] Restore pre-check: Moodle version...
[10/10/24, 23:03:25] [info] [pid 1049915] ...OK
[10/10/24, 23:03:25] [info] [pid 1049915] Restore pre-check: Add-on plugins...
[10/10/24, 23:03:26] [info] [pid 1049915] ...OK
[10/10/24, 23:03:26] [info] [pid 1049915] Restore pre-check: Disk space...
[10/10/24, 23:03:26] [info] [pid 1049915] ...OK
[10/10/24, 23:03:26] [info] [pid 1049915] Restore pre-check: Environment check...
[10/10/24, 23:03:26] [info] [pid 1049915] ...OK
[10/10/24, 23:03:45] [info] [pid 1049915] Restore started
[10/10/24, 23:03:45] [info] [pid 1049915] !!!! Callback tool_testcallback_tool_vault_restore in the stage 'before'
[10/10/24, 23:03:45] [info] [pid 1049915] Purging caches...
[10/10/24, 23:03:45] [info] [pid 1049915] ...done
[10/10/24, 23:03:45] [info] [pid 1049915] Making list of the old files...
[10/10/24, 23:03:45] [info] [pid 1049915] ...done
[10/10/24, 23:03:45] [info] [pid 1049915] Starting database restore (443 tables)...
[10/10/24, 23:03:45] [info] [pid 1049915] Downloading file dbdump.zip ...
[10/10/24, 23:03:46] [info] [pid 1049915] ...done
[10/10/24, 23:04:01] [info] [pid 1049915] Restored 358/443 tables,     2.9MB/3MB ( 97)%
[10/10/24, 23:04:04] [info] [pid 1049915] Restored 443/443 tables,       3MB/3MB (100)%
[10/10/24, 23:04:04] [info] [pid 1049915] Finished database restore
[10/10/24, 23:04:04] [info] [pid 1049915] !!!! Callback tool_testcallback_tool_vault_restore in the stage 'afterdb'
[10/10/24, 23:04:04] [info] [pid 1049915] Killing all sessions...
[10/10/24, 23:04:04] [info] [pid 1049915] ...done
[10/10/24, 23:04:04] [info] [pid 1049915] Purging caches...
[10/10/24, 23:04:04] [info] [pid 1049915] ...done
[10/10/24, 23:04:04] [info] [pid 1049915] Rebuilding $CFG...
[10/10/24, 23:04:04] [info] [pid 1049915] ...done
[10/10/24, 23:04:04] [info] [pid 1049915] Recalculating all versions hash...
[10/10/24, 23:04:04] [info] [pid 1049915] ...done
[10/10/24, 23:04:04] [info] [pid 1049915] Starting dataroot restore
[10/10/24, 23:04:04] [info] [pid 1049915] Finished dataroot restore
[10/10/24, 23:04:04] [info] [pid 1049915] !!!! Callback tool_testcallback_tool_vault_restore in the stage 'afterdata'
[10/10/24, 23:04:04] [info] [pid 1049915] Starting files restore
[10/10/24, 23:04:04] [info] [pid 1049915] Downloading file filedir.zip ...
[10/10/24, 23:04:06] [info] [pid 1049915] ...done
[10/10/24, 23:04:08] [info] [pid 1049915] Finished files restore
[10/10/24, 23:04:08] [info] [pid 1049915] !!!! Callback tool_testcallback_tool_vault_restore in the stage 'afterall'
[10/10/24, 23:04:08] [info] [pid 1049915] Removing old files...
[10/10/24, 23:04:08] [info] [pid 1049915] ...done
[10/10/24, 23:04:08] [info] [pid 1049915] Restore finished
```