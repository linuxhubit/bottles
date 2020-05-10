gtk_sharp_dep = dependency('gtk-sharp-3.0')

bottles_sources = [
  'main.cs',
]

executable('bottles', bottles_sources,
  dependencies: gtk_sharp_dep,
       install: true,
   install_dir: join_paths(get_option('prefix'), 'libexec'),
)

cdata = configuration_data()
cdata.set('libexecdir', join_paths(get_option('prefix'), 'libexec'))
configure_file(
          input: 'bottles.in',
         output: 'bottles',
  configuration: cdata,
        install: true,
    install_dir: get_option('bindir'),
)
