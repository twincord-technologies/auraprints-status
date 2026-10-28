# AuraPrints status monitor

A scheduled GitHub Actions workflow ([site-monitor.yml](.github/workflows/site-monitor.yml)) that checks the public
AuraPrints pages every 10 minutes. A page counts as down only after two failed checks 4 minutes apart; the run then
fails and GitHub emails the maintainers.

This repository holds no code and no secrets: only the workflow and the public URLs it checks. Runs are best effort
(GitHub may start scheduled runs late). A monthly empty "keepalive" commit keeps the schedule active.

To test the alert email: *Actions → Site monitor → Run workflow* with **Alert test** ticked.
