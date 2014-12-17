# imgup

Server for storing images copied from your filesystem or over HTTP.

## RestClient examples

Copy from filesystem

	RestClient.post(
      'http://your.imgup.server/upload',
      :file => '/fs/path/to/file.jpg'
    )

Copy over HTTP

	RestClient.post(
	  'http://your.imgup.server/src',
	  :src => 'http://www.some.domain/path/to/file.jpg
	)

Retrieve image

	RestClient.get( 'http://your.imgup.server/upload/2015/JAN/file.jpg' )

Retrieve image exif data as JSON

	RestClient.get( 'http://your.imgup.server/upload/2015/JAN/file.jpg?cmd=exif' )