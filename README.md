# IPTVM3U


Hybrid list adapted for kodi using different addons to make the stream work

all Playlist work with the Playlistloader addon  for kodi 18.9 or 19+ matrix as exception of Streamlink Tester  since some dependencies are not ported to python 3 yet


################

will no longer be used for live ,to mutch time consuming to keep it updated ... only good For Direct Video only
# Youtube : Video Id :  No API required : link Update required (UPD)
#EXTINF:-1 tvg-logo="" group-title="", (YT) (v_id) (UPD)
plugin://plugin.video.youtube/play/?video_id=IDHERE

will be used for those who have the api
# Youtube : Channel ID : API required : No Update required
#EXTINF:-1 tvg-logo="" group-title="", (YT) (c_id)
plugin://plugin.video.youtube/play/?channel_id=IDHERE&live=1

If Multiple Live From The same Channel , Change &live=2 ... and so on  need to be tested to fit the Channel Naming

https://blog.hubspot.com/website/how-to-get-youtube-api-key


################


# Twitch : Channel Name
#EXTINF:-1 tvg-logo="" group-title="", (TWITCH) (C_N)
plugin://plugin.video.twitch/?mode=play&channel_name=

# Twitch : Channel ID
#EXTINF:-1 tvg-logo="" group-title="", (TWITCH) (C_id)
plugin://plugin.video.twitch/?channel_id=IDHERE&amp;mode=play

Twitch Channel ID can be found from the site , in The m3u8 link , detected by a hsl or m3u8 stream detector , as per exemple  . Download helper plugin in firefox
you will find link that begin by https://usher.ttvnw.net/api/channel/hls/?????.m3u8? + A long Token .. in the token search : channel_id String

exemple: https://www.twitch.tv/asot = channel_id%22%3A265735182%2C%22  , the id  will be 265735182

################

**** Token Retreivers ****

# Streamlink Tester

#EXTINF:-1 tvg-logo="" group-title="",  (SLT)
plugin://plugin.video.streamlink-tester/?action=play&url=URLHERE

Usefull For many  Site That Use .php ending  EX: .php?id=IDHERE

- DASH .mpd Stream  No DMR + No Referrer

https://streamlink.github.io/plugin_matrix.html

# Tested  WebSite :

https://piczel.tv/watch/CHANNELNAMEHERE

https://goodgame.ru/channel/CHANNELNAMEHERE

http://www.giniko.com/ ; http://www.giniko.com/watch.php?id=IDHERE

https://ginikousa.com/ ; https://ginikousa.com/live.php?id=IDHERE

https://www.watchyour.tv/ ; http://www.watchyour.tv/dvr.php?id=IDHERE

# Send To Kodi  
18.9 or matrix see here https://github.com/firsttris/plugin.video.sendtokodi

#EXTINF:-1 tvg-logo="" group-title="", (STK)
plugin://plugin.video.sendtokodi/?URLHERE

# Tested  WebSite :

https://fb.watch/IDHERE/

https://www.facebook.com/IDHERE/videos/IDEHERE/

https://www.youtube.com/channel/IDHERE/live ->  No youtube API required to make it work .. handle 1 unique live from same channel

https://www.youtube.com/watch?v=IDHERE

https://www.dailymotion.com/video/IDHERE

https://www.twitch.tv/CHANNELNAMEHERE

https://www.veoh.com/watch/IDHERE

https://vimeo.com/IDHERE

https://ok.ru/live/IDHERE|User-Agent=Mozilla/5.0 (Linux; Android 10) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/87.0.4280.101 Mobile Safari/537.36

https://ok.ru/video/IDHERE|User-Agent=Mozilla/5.0 (Linux; Android 10) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/87.0.4280.101 Mobile Safari/537.36

https://dlive.tv/CHANNELNAMEHERE

https://livestream.com/accounts/IDHERE/events/IDHERE

https://picarto.tv/CHANNELNAMEHERE


################


# Dailymotion : LIVE Only
#EXTINF:-1 tvg-logo="" group-title="", (DM)
plugin://plugin.video.dailymotion_com/?url=IDHERE&amp;mode=playLiveVideo

# Dailymotion : VOD Only
#EXTINF:-1 tvg-logo="" group-title="", (DM_VOD)
plugin://plugin.video.dailymotion_com/?mode=playVideo&url=IDHERE

################

# Dailymotion : VLC Only
#EXTINF:-1 tvg-logo="" group-title="", (For VLC)
https://www.dailymotion.com/video/IDHERE#tab_embed.m3u8


################

HLS Stream URL option can be Required and tricked by using

# User-Agent=
|User-Agent=
# Most Common
|User-Agent=stream
|User-Agent=VLC
|User-Agent=Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4472.124 Safari/537.36
# More Here
http://useragentstring.com/pages/useragentstring.php?name=All
# Referer=
|Referer=
Url Referer of the .m3u8 Stream
# X-Forwarded-For=
|X-Forwarded-For=
Usaly It work without a vpn  by simply finding the proper ISP ip/range of the country that match the geo restriction Stream




