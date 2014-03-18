# flickr-commons-metadata

flickr-commons-metadata contains the raw metadata for Flickr Commons photos in JSON format pulled from the Flickr API using the following methods:

* [flickr.photos.getInfo](http://www.flickr.com/services/api/flickr.photos.getInfo)
* [flickr.photos.getSizes](http://www.flickr.com/services/api/flickr.photos.getSizes)
* [flickr.photos.comments.getList](http://www.flickr.com/services/api/flickr.photos.comments.getList)
* [flickr.photos.getAllContexts](http://www.flickr.com/services/api/flickr.photos.getAllContexts)
* [flickr.photos.getExif](http://www.flickr.com/services/api/flickr.photos.getExif) _– if publicly available_

For example:

	$>ls -al data/83979593@N00/224/682/902/*
	-rw-r--r--  1 asc  staff    53 Dec 20 15:49 83979593@N00/224/682/902/224682902-c.json
	-rw-r--r--  1 asc  staff   255 Dec 20 15:49 83979593@N00/224/682/902/224682902-ctx.json
	-rw-r--r--  1 asc  staff  7952 Dec 20 15:49 83979593@N00/224/682/902/224682902-e.json
	-rw-r--r--  1 asc  staff  2273 Dec 20 15:49 83979593@N00/224/682/902/224682902-i.json
	-rw-r--r--  1 asc  staff  2060 Dec 20 15:49 83979593@N00/224/682/902/224682902-s.json

As of mid-morning December 21 (2013) metadata files contain a
`flarchive:created` attribute which is a Unix timestamp indicating when the file
was last archived.

For example:

	$> cat 6260452122-i.json | python -mjson.tool
	{
	    "flarchive:created": 1387636691,
	    "photo": {
        	"comments": {
   	         "_content": "0"
        	},
	    ... and so on
	}

_That means as of mid-morning December 21 (2013) a bunch of metadata files
archived before this date are still missing the `flarchive:created` attribute._

## Details

Individual institutions are archived using the
[py-flarchive](https://github.com/straup/py-flarchive) library, like this:

	$> python ./flarchive/__init__.py -v -a <APIKEY> -n <NSID> -d flickr-commons-metadata/data

This is a _massive_ repository and it's not at all clear that the way the data has been organized is the best way to do things. This is a first pass just to get the data and once that's done some time spent re-thinking how and where the data is stored is in order.

## Institutions

### In process

The following institutions are currently being archived by one or more people

* _nothing right now_

_If you are archiving one or more institutions below add them here and send me a pull request or open an issue and I will add it to the list._

### Complete list

* [Australian National Maritime Museum on The Commons](data/33147718%40N05) - _last archived 20131223_
* [Australian War Memorial collection](data/30115723@N02) – _last archived 20131228_
* [Bergen Public Library](data/37381115@N04) – _last archived 20131224_
* [bibliothequedetoulouse](data/26134435@N05) – _last archived 20131228_
* [Biblioteca de Arte-Fundação Calouste Gulbenkian](data/26577438%40N06) – _last archived 20131222_
* [Brooklyn Museum](data/83979593%40N00) – _last archived 20131220_
* [California Historical Society Digital Collection](data/99278405%40N04) – _last archived 20131222_
* [Center for Jewish History, NYC](data/36988361@N08) – _last archived 20140102_
* [Cornell University Library](data/30515687@N05) – _last archived 20140113_
* [Costică Acsinte Archive](data/109550159%40N08) – _last archived 20131223_
* [DC Public Library Commons](data/36038586%40N04) – _last archived 201403_
* [DEXTRA Photo](data/88669438@N03) – _last archived 20131228_
* [Deseronto Archives](data/23121382@N07) – _last archived 20140108_
* [Dundas Museum and Archives](data/39758725@N03)_last archived 20131228_
* [Fylkesarkivet i Sogn og Fjordane](data/37547255@N08) – _last archived 20140102_
* [Galt Museum & Archives on The Commons](data/23686862@N03) – _last archived 20131228_
* [George Eastman House](data/7167652%40N06) – _last archived 20131222_
* [Getty Research Institute](data/35532303@N08) – _last archived 20131228_
* [Het Nieuwe Instituut - Architecture Collection](data/47154409%40N06) – _last archived 20131221_
* [IWM Collections](data/32300107@N06) – _last archived 20140102_
* [JWA Commons](data/36281769@N04) – _last archived 20131228_
* [Jewish Historical Society of the Upper Midwest](data/48143042@N05) – _last archived 20131229_
* [Keene and Cheshire County (NH) Historical Photos](data/25960495@N06) – _last archived 20140113_
* [LSE Library](data/35128489%40N07) – _last archived 20131223_
* [Law Society of Upper Canada Archives](data/38561291%40N04) – _last archived 20131223_
* [Ljósmyndasafn Reykjavíkur / Reykjavík Museum of](data/9189488@N02) – _last archived 20131224_
* [LlGC ~ NLW](data/37199428@N06) – _last archived 20140108_
* [Mennonite Church USA Archives](data/52529054@N06) – _last archived 20140113_
* [Miami University Libraries - Digital Collections](data/31033598@N03) – _last archived 20140311_
* [Mississippi Department of Archives and History](data/77015680%40N05)  – _partially archived as of 20131223_
* [Musée McCord Museum](data/25786829%40N08) – _last archived 20131220_
* [Museum of Hartlepool](data/47908901@N03) – _last archived 20131224_
* [Museum of Photographic Arts Collections](data/61498590@N03) – _last archived 20140102_
* [NASA on The Commons](data/44494372%40N05) – _last archived 20131221_
* [Nationaal Archief](data/29998366%40N02) – _last archived 20131222_
* [National Archives of Estonia](data/94021017@N05) – _last archived 20131222_
* [National Galleries of Scotland Commons](data/30835311@N07) – _last archived 20131222_
* [National Library NZ on The Commons](data/32741315%40N06) – _last archived 20131220_
* [National Library of Australia Commons](data/67193564@N03) – _last archived 20140102_
* [National Library of Ireland on The Commons](data/47290943@N03) – _last archived 20131224_
* [National Library of Norway](data/48220291@N04) – _last archived 20131223_
* [National Library of Scotland](data/14456531@N07) – _last archived 20131222_
* [National Library of Sweden](data/95520404@N07) – _last archived 20131223_
* [National Maritime Museum](data/11334970%40N05) – _last archived 20131222_
* [National Media Museum](data/26808453@N03) – _last archived 20140102_
* [National Museum of Denmark](data/95772747%40N07) – _last archived 20131222_
* [New York Public Library](data/32951986%40N05) – _last archived 20131221_
* [nha.library](data/34101160@N07) – _last archived 20131228_
* [Nova Scotia Archives](data/61232251@N05) – _last archived 20131228_
* [OSU Special Collections & Archives : Commons](data/34586311@N05) – _last archived 20140113_
* [Powerhouse Museum Collection](data/24785917%40N03) – _last archived 20131220_
* [Provincial Archives of Alberta](data/95711690@N03) – _last archived 20140311_
* [Public Record Office of Northern Ireland](data/54403180@N04) – _last archived 20131224_
* [The British Library](data/12403504%40N02) - _last archived 20140316_
* [Nationaal Archief](data/29998366%40N02) – _last archived 20131222_
* [bibliothequedetoulouse](data/26134435@N05) – _last archived 20131228_
* [California Historical Society Digital Collection](data/99278405%40N04) – _last archived 20131222_
* [Law Society of Upper Canada Archives](data/38561291%40N04) – _last archived 20131223_
* [Vancouver Public Library Historical Photographs](data/99915476%40N04) – _last archived 20131223_
* [The Library of Virginia](data/30194653@N06) – _last archived 20140102_
* [Riksarkivet (National Archives of Norway)](data/59811348@N05) – _last archived 20131223_
* [Royal Australian Historical Society](data/69269002@N04) – _last archived 20131228_
* [SMU Central University Libraries](data/41131493@N06) – _last archived 20140113_
* [San Diego Air & Space Museum Archives](data/49487266%40N07) – _last archived 20140115_
* [Schlesinger Library, RIAS, Harvard University](data/99902797@N03) – _last archived 20140102_
* [Smithsonian Institution](data/25053835%40N03) – _last archived 20131220_
* [State Library and Archives of Florida](data/31846825%40N04) – _last archived 20131222_
* [State Library of New South Wales collection](data/29454428%40N08) - _last archived 20140116_
* [State Library of Queensland, Australia](data/32605636@N06) – _last archived 20140113_
* [Biblioteca de Arte-Fundação Calouste Gulbenkian](data/26577438%40N06) – _last archived 20131222_
* [The Library of Congress](data/8623220%40N02) – _last archived 20131221_
* [Royal Australian Historical Society](data/69269002@N04) – _last archived 20131228_
* [DC Public Library Commons](data/36038586@N04) – _last archived 20140308_
* [Fylkesarkivet i Sogn og Fjordane](data/37547255@N08) – _last archived 20140102_
* [New York Public Library](data/32951986%40N05) – _last archived 20131221_
* [Riksarkivet (National Archives of Norway)](data/59811348@N05) – _last archived 20131223_
* [Australian War Memorial collection](data/30115723@N02) – _last archived 20131228_
* [State Records NSW](data/27331537@N06) – _last archived 20140113_
* [Stockholm Transport Museum Commons](data/62173425%40N02) – _last archived 20131221_
* [Svenska litteratursällskapet i Finland](data/48641766%40N05) – _last archived 20131221_
* [Swedish National Heritage Board](data/34419668@N08) – _last archived 20131223_
* [Texas State Archives](data/47326604@N02) – _last archived 20140110_
* [The Field Museum Library](data/35310696@N04) – _last archived 20140110_
* [The Library of Congress](data/8623220%40N02) – _last archived 20131221_
* [The Library of Virginia](data/30194653@N06) – _last archived 20140102_
* [The National Archives UK](data/31575009@N05) – _last archived 20131224_
* [The Royal Library, Denmark](data/45270502@N06) – _last archived 20131222_
* [The U.S. National Archives](data/35740357%40N03) – _last archived 20131222_
* [Tyne & Wear Archives & Museums](data/29295370%40N07) - _last archived 20140116_
* [UA Archives | Upper Arlington History](data/37784107@N08) – _last archived 20131228_
* [UL Digital Library](data/95717549@N07) – _last archived 20131229_
* [UW Digital Collections](data/8337233@N06) – _last archived 20140102_
* [Vancouver Public Library Historical Photographs](data/99915476%40N04) – _last archived 20131223_
* [Woodrow Wilson Presidential Library Archives](data/41815917@N06) – _last archived 20140102_
* [Tasmanian Archive and Heritage Office](data/79256815%40N03) – _last archived 20140318_
* [Library Company of Philadelphia](data/26491575%40N05)  – _last archived 20140318_

## Contributors

* @straup
* @hugovk

## See also

* [py-flarchive](https://github.com/straup/py-flarchive)

