project('cairo_jpg', 'c', version: '0.0.1')

lib = library(
  'cairo_jpg',
  'src/cairo_jpg.c',
  dependencies: [
    dependency('cairo', fallback: ['cairo', 'cairo_dep']),
    dependency('libjpeg', fallback: ['libjpeg-turbo', 'libturbojpeg_dep']),
  ],
  install: true,
)
install_headers('src/cairo_jpg.h')
pkg = import('pkgconfig')
pkg.generate(lib)

cairo_jpg_dep = declare_dependency(link_with: lib, include_directories: [include_directories('src')])
