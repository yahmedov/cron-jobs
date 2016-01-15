1. copy the shell scripts to /home/medenkac/bin ;
2. Set cron jobs as follow
	0 * * * * /home/medenkac/bin/mk-http-log.sh
	0 1 * * * /home/medenkac/bin/rm-old-http-logs.sh
	10 16 * * * /home/medenkac/bin/rename-log-file.sh
	
/*
This will:
	create log files in http://medenka.com/access-logs/
	update log file - every day, every hour
	remove old files (older than 20 days) - every day at 1am
	create second part of the log file for a day - every day at 16:10
*/
	
