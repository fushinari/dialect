project('dialect',
          version: '0.0.0',
    meson_version: '>= 0.50.0',
  default_options: [ 'warning_level=2',
                   ],
)

python = import('python3')

message('Looking for dependencies')
python_bin = python.find_python()
if not python_bin.found()
    error('No valid python3 binary found')
else
    message('Found python3 binary')
endif

dependency('gobject-introspection-1.0', version: '>= 1.35.0')
dependency('gtk+-3.0', version: '>= 3.22')
dependency('glib-2.0')
dependency('pygobject-3.0', version: '>= 3.29.1')

subdir('data')
subdir('src')

meson.add_install_script('build-aux/meson/postinstall.py')
