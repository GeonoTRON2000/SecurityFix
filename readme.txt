##
##
##        Mod title:  Security Fix
##
##      Mod version:  1.0
##  Works on FluxBB:  1.5.3
##     Release date:  2013-09-14
##           Author:  GeonoTRON2000
##
##      Description:  Applies the security fix from FluxBB 1.5.4 to FluxBB 1.5.3.
##
##   Affected files:  misc.php
##
##       Affects DB:  No
##
##
##       DISCLAIMER:  Please note that "mods" are not officially supported by
##                    FluxBB. Installation of this modification is done at your
##                    own risk. Backup your forum database and any and all
##                    applicable files before proceeding.
##
##


#
#---------[ 1. OPEN ]-------------------------------------------------------
#

misc.php


#
#---------[ 2. FIND (line: 100) ]----------------------------------------------------------
#

	if (isset($_POST['form_sent']))
	{
		// Clean up message and subject from POST
		$subject = pun_trim($_POST['req_subject']);
		$message = pun_trim($_POST['req_message']);


#
#---------[ 3. REPLACE WITH ]-------------------------------------------------------
#

	if (isset($_POST['form_sent']))
	{
		confirm_referrer('misc.php');

		// Clean up message and subject from POST
		$subject = pun_trim($_POST['req_subject']);
		$message = pun_trim($_POST['req_message']);


#
#---------[ 4. SAVE/UPLOAD ]-------------------------------------------------
#