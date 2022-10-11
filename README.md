# Before we begin
Before we begin you should do following things.

Make sure that you install termux-api
Now you should give notifications permission to termux-api.
termux-notification-list
After running above command in termux,click Allow.
Then run termux-notificatin-list and see a json is showing or not. If it's not shown try enabling Auto Start for Termux:API and disable all battery optimizations. https://dontkillmyapp.com/xiaomi
Make sure that you install git and make.
# installing and Login
First clone this repository.

git clone https://github.com/sumithemmadi/truecaller-on-termux.git
cd truecaller-on-termux
make install
Then login to your Truecaller account.

After installation you need to restart session or source this file:

source start-truecallerjs.sh
Now you ready to enable and start the truecallerjs daemon service:

sv-enable truecallerjs
sv up truecallerjs
If you need to stop, run sv down truecallerjs

Note : If you get any error just close the termux app and reopen it.Then start truecallerjs services. Note : If it is not working export the exvironment variable DEFAULT_DIALER_APP="Yor Dialer App Package Name" .

click here to know about package name
export DEFAULT_DIALER_APP="Yor Dialer App Package Name"
Example 1: If you use MI Dialer which has a package name com.android.incalleriu.

~$ export DEFAULT_DIALER_APP="com.android.incalleriu"
# To uninstall
make uninstall
Then stop service with below command

sv down truecallerjs
sv-disable truecallerjs
