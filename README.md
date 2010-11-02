# Raphaël-ZPD
### A little plugin for the Raphaël Javascript SVG library enabling canvas-wide zoom, pan and drag functionality.

## Usage
Create a Raphaël paper object, then call the ZPD initialization function with the systems to enable (before performing any drawing operations):

	$ paper.ZPD({ zoom: true, pan: true, drag: true });

Repeated calls to this function may be used to alter the settings as needed. You may disable the drag functionality on the basis of individual Raphaël elements like so:

	$ el.node.draggable = false;

## Potential Issues

Note that the ZPD function will create an SVG group element ('viewport') and alter the paper's canvas to point it, causing all following elements created by Raphaël to be placed within. This will potentially break any plugins or Raphaël functions that rely on paper.canvas pointing to the root SVG object, though I have yet to encounter such a situation.

## Acknowledgements

Based on the [SVGPan](http://code.google.com/p/svgpan/) library created by Andrea Leofreddi.

## License

Copyright 2010 Daniel Assange <somnidea@lemma.org> (Raphaël integration and extensions). All rights reserved.

Copyright 2009-2010 Andrea Leofreddi <a.leofreddi@itcharm.com> (original author). All rights reserved.

Redistribution and use in source and binary forms, with or without modification, are
permitted provided that the following conditions are met:

   1. Redistributions of source code must retain the above copyright notice, this list of
      conditions and the following disclaimer.

   2. Redistributions in binary form must reproduce the above copyright notice, this list
      of conditions and the following disclaimer in the documentation and/or other materials
      provided with the distribution.

THIS SOFTWARE IS PROVIDED BY Andrea Leofreddi ``AS IS'' AND ANY EXPRESS OR IMPLIED
WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND
FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL Andrea Leofreddi OR
CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR
CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR
SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON
ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING
NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF
ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

The views and conclusions contained in the software and documentation are those of the
authors and should not be interpreted as representing official policies, either expressed
or implied, of Andrea Leofreddi.
