# wavplot : read and plot channels of a WAV file

wavplot reads a WAV file and uses matplotlib to plot the signal(s) contained in it to either file or the screen.

## Installation

Dependencies:

    * numpy
    * matplotlib

Given presence of the above, just clone the repo or copy the wavplot (Python 2.7) file to your machine. Edit execute permissions if necessary, and call it (see examples below).

![Example wavplot output](https://raw.github.com/ninly/wavplot/example.png)

## Usage

    $ ./wavplot [-v[v]] [--start FIRSTSAMP] [--end LASTSAMP] [--channels X [Y Z ...]] [--show] wavfile

Use ./wavplot --help for more information, or see the examples below.

### Examples

    $ ./wavplot myfile.wav

Read and plot all channels in myfile.wav, and write the plot to plot.png.

    $ ./wavplot --start 10 --end 50 myfile.wav

Read and plot samples 10-50 (inclusive) of all channels in myfile.wav, and write to plot.png.

    $ ./wavplot --channels 2 myfile.wav

Read and plot all of channel 2 (of 2) of myfile.wav, and write to plot.png.

    $ ./wavplot --start 100 --end 200 --channels 2 3 5 myfile.wav

Read and plot samples 100-200 of channel 2, 3, and 5 of myfile.wav, and write to plot.png.

    $ ./wavplot -o niceplot.png myfile.wav

Read and plot all of myfile.wav, and write to niceplot.png. Typing "--plotfile niceplot.png" also works.

Add "--show" to any of the above to display the plot on screen instead of writing to a file.

## Contributing

1. Fork it!
2. Create your feature branch:`git checkout -b my-new-feature`
3. Commit your changes: git commit -am 'Add some feature'`
4. Push to the branch: git push origin my-new-feature`
5. Submit a pull request...

## History

### 13 February 2015

Initial commit

## Credits

Author: Jason Conklin (@ninly).

Thanks to Steve Conklin (@sconklin).

## License

MIT. See LICENSE file.
