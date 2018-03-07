RAI.TV API
==========

C'era una volta la app RaiTV, ma adesso è stata sostituita da RaiPlay ed anche questa bella pagina è destinata ad essere rimpiazzata. Anzi, è già successo! [raiapi](https://github.com/maxcanna/raiapi) e [raiplay_fetcher](https://github.com/giuscri/raiplay_fetcher).

## Ricevere informazioni sui canali

http://www.rai.tv/dl/RaiTV/iphone/android/smartphone/advertising_config.html

Return a JSON:

- Channels
    + object
        * __diretta__
        * __direttaLink__
        * __direttaLink2__
        * __hasReplay__
        * __hexColor__
        * __icon__
        * __iconSize__
        * __id__
        * __image__
        * __name__
        * __parsePlaylist__
        * __preroll_location_diretta__
        * __tag__
        * __weblink__
- RayReplay
    + object
        * __base__
- adv_resume_limit
- adv_resume_limit_inuse
- advertising_active
- advertising_banner_baseurl
- advertising_inter_baseurl
- advertising_preroll_baseurl
- advertising_timers
    + object
        * __RAIAdvBanner__
        * __RAIAdvInterstitial__
        * __RAIAdvVideo__
-  advertising_watcher_active
-  alert
    +  object
        *  __active__
        *  __text__
        *  __url__
        *  __version__
- analytics_domain
- analytics_url
- banner_dirette_location
- banner_home_location
- banner_replay_location
- banner_vod_location
- baseUrl
- beanCounter
    + additional_search
        * Pi\u00c3\u0192\u00c6\u2019\u00c3\u201a\u00c2\u00b9 Popolari
    + api_endpoint
    + api_endpoint_test
    + __api_key__
    + services



## Ottenere i programmi in onda
lo URL da chiamare è http://www.rai.it/PalinsestiNeoFE/getJson.do?action=getDirette&canali=

Dobbiamo aggiungere in fondo l'id del canale
### I canali della RAI vengono indicati con questi id

Id  | Canale
----|-------
1   | Rai uno
2   | Rai due
3   | Rai tre
41  | Rai quattro
31  | Rai Extra
25  | Rai News24 
26  | Rai Sport Satellite
43  | Rai sport 2
32  | Rai Premium
28  | Rai Storia
38  | Rai yoyo
23  | Rai gulp
33  | Cinema World
24  | Rai Educational
21 | Sat 2000
35 | Rai 1 mobile
36 | Rai 2 mobile
37 | Rai 3 mobile
42 | Euronews
49 | Rai Italia 1
50 | Rai Italia 2 Australia
51 | Rai Italia 3
52 | Gr Parlamento
53 | Rai Italia 2 Asia
54 | FVG TV ITA
55 | FVG TV SLO


Viene restituiro un JSON

- Dirette
    + object
        * idcanale
        * nomeCanale
        * id
        * date
        * hour
        * length
        * name
        * desc
        * descProgram
        * from
        * idprogramma
        * image


## Informazioni sul replay

http://www.rai.it/dl/portale/html/palinsesti/replaytv/static/RaiUno_2014_10_23.html

- now
- defaultBannerVars
    + object
- 1
    + aaaa-mm-dd
        * hh:mm
            - t
            - d
            - l
            - r
            - e
            - image
            - h264
            - h264_400
            - h264_600
            - h264_800
            - h264_1200
            - h264_1500
            - h264_1800
            - urltablet
            - urlrisorsasottotitoli
            - urlrisorsahighlights
            - urlrisorsatagli
            - urlSmartPhone
            - dash
            - i
            - a
            - aDate
            - endDate
            - s
            - w
            - v
            - idProgramma
            - nomeProgramma
            - dir1
            - dir2
            - dir3
            - dir4
            - dir5
            - bsk
            - b250
            - b100
            - bsp

## Informazioni sull'on-Demand

http://www.rai.tv/StatisticheProxy/proxyPost.jsp?action=getLastContentByTag&numContents=30&type=Video&tags=Tematica:Cartoni&domain=RaiTv&xsl=rai_tv-statistiche-iphone&excludeTags=Tematica:News%5ETematica:ntz

- name
- setId
- pages
- currPage
- pageType
- b100
- b250
- bsp
- list
    + Array
        * Obj
            - type
            - itemId
            - webLink
            - mediaUri
            - h264
            - m3u8
            - image
            - image_medium
            - image_300
            - image_433
            - length
            - date
            - name
            - author
            - from
            - editore
            - desc
            - bsp
            - b100
            - b250











