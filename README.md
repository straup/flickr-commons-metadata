# flickr-commons-metadata

flickr-commons-metadata contains the raw metadata for Flickr Commons photos in JSON format pulled from the Flickr API using the following methods:

* [flickr.photos.getInfo](http://www.flickr.com/services/api/flickr.photos.getInfo)
* [flickr.photos.getSizes](http://www.flickr.com/services/api/flickr.photos.getSizes)
* [flickr.photos.comments.getList](http://www.flickr.com/services/api/flickr.photos.comments.getList)
* [flickr.photos.getAllContexts](http://www.flickr.com/services/api/flickr.photos.getAllContexts)
* [flickr.photos.getExif](http://www.flickr.com/services/api/flickr.photos.getExif)

For example:

	$>ls -al data/83979593@N00/224/682/902/*
	-rw-r--r--  1 asc  staff    53 Dec 20 15:49 83979593@N00/224/682/902/224682902-c.json
	-rw-r--r--  1 asc  staff   255 Dec 20 15:49 83979593@N00/224/682/902/224682902-ctx.json
	-rw-r--r--  1 asc  staff  7952 Dec 20 15:49 83979593@N00/224/682/902/224682902-e.json
	-rw-r--r--  1 asc  staff  2273 Dec 20 15:49 83979593@N00/224/682/902/224682902-i.json
	-rw-r--r--  1 asc  staff  2060 Dec 20 15:49 83979593@N00/224/682/902/224682902-s.json

## Details

Not all (read: most) participating institutions have been added to the
repository yet so contributions and pull requests are welcome.

Individual institutions are archived using the
[py-flarchive](https://github.com/straup/py-flarchive) library, like this:

	$> python ./flarchive/__init__.py -v -a <APIKEY> -n <NSID> -d flickr-commons-metadata/data

## Institutions

* [Musée McCord Museum](data/25786829%40N08) – _last archived 20131220_
* Cornell University Library	(30515687@N05)
* National Maritime Museum	(11334970@N05)
* Australian National Maritime Museum on The Commons	(33147718@N05)
* Texas State Archives	(47326604@N02)
* SMU Central University Libraries	(41131493@N06)
* nha.library	(34101160@N07)
* Stockholm Transport Museum Commons	(62173425@N02)
* National Library of Ireland on The Commons	(47290943@N03)
* UL Digital Library	(95717549@N07)
* National Media Museum	(26808453@N03)
* UA Archives | Upper Arlington History	(37784107@N08)
* Getty Research Institute	(35532303@N08)
* National Library of Sweden	(95520404@N07)
* Center for Jewish History, NYC	(36988361@N08)
* [Smithsonian Institution](data/25053835%40N03) – _last archived 20131220_
* The U.S. National Archives	(35740357@N03)
* OSU Special Collections & Archives : Commons	(34586311@N05)
* The Royal Library, Denmark	(45270502@N06)
* Mennonite Church USA Archives	(52529054@N06)
* The National Archives UK	(31575009@N05)
* Ljósmyndasafn Reykjavíkur / Reykjavík Museum of	(9189488@N02)
* [Brooklyn Museum](data/83979593%40N00) – _last archived 20131220_
* Keene and Cheshire County (NH) Historical Photos	(25960495@N06)
* The Field Museum Library	(35310696@N04)
* National Galleries of Scotland Commons	(30835311@N07)
* Jewish Historical Society of the Upper Midwest	(48143042@N05)
* Het Nieuwe Instituut - Architecture Collection	(47154409@N06)
* National Library of Norway	(48220291@N04)
* National Museum of Denmark	(95772747@N07)
* Tyne & Wear Archives & Museums	(29295370@N07)
* Dundas Museum and Archives	(39758725@N03)
* Bergen Public Library	(37381115@N04)
* National Library of Scotland	(14456531@N07)
* National Archives of Estonia	(94021017@N05)
* San Diego Air & Space Museum Archives	(49487266@N07)
* Museum of Hartlepool	(47908901@N03)
* State Library and Archives of Florida	(31846825@N04)
* LSE Library	(35128489@N07)
* Deseronto Archives	(23121382@N07)
* LlGC ~ NLW	(37199428@N06)
* Swedish National Heritage Board	(34419668@N08)
* Nova Scotia Archives	(61232251@N05)
* Public Record Office of Northern Ireland	(54403180@N04)
* The British Library	(12403504@N02)
* Nationaal Archief	(29998366@N02)
* bibliothequedetoulouse	(26134435@N05)
* California Historical Society Digital Collection	(99278405@N04)
* Law Society of Upper Canada Archives	(38561291@N04)
* Vancouver Public Library Historical Photographs	(99915476@N04)
* The Library of Virginia	(30194653@N06)
* State Library of New South Wales collection	(29454428@N08)
* JWA Commons	(36281769@N04)
* Costică Acsinte Archive	(109550159@N08)
* DEXTRA Photo	(88669438@N03)
* National Library of Australia Commons	(67193564@N03)
* Museum of Photographic Arts Collections	(61498590@N03)
* State Library of Queensland, Australia	(32605636@N06)
* Biblioteca de Arte-Fundação Calouste Gulbenkian	(26577438@N06)
* [The Library of Congress](data/8623220%40N02)
* Royal Australian Historical Society	(69269002@N04)
* DC Public Library Commons	(36038586@N04)
* Fylkesarkivet i Sogn og Fjordane	(37547255@N08)
* [New York Public Library](data/32951986%40N05)
* Riksarkivet (National Archives of Norway)	(59811348@N05)
* Australian War Memorial collection	(30115723@N02)
* State Records NSW	(27331537@N06)
* UW Digital Collections	(8337233@N06)
* George Eastman House	(7167652@N06)
* Schlesinger Library, RIAS, Harvard University	(99902797@N03)
* NASA on The Commons	(44494372@N05)
* IWM Collections	(32300107@N06)
* Galt Museum & Archives on The Commons	(23686862@N03)
* Svenska litteratursällskapet i Finland	(48641766@N05)
* Woodrow Wilson Presidential Library Archives	(41815917@N06)
* [Powerhouse Museum Collection](data/24785917%40N03) – _last archived 20131220_
* Mississippi Department of Archives and History	(77015680@N05)
* [National Library NZ on The Commons](data/32741315%40N06) – _last archived 20131220_

## See also

* [py-flarchive](https://github.com/straup/py-flarchive)
