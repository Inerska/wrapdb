add_languages('c')

executable(
  'openal-info',
  'openal-info.c',
  dependencies: openal_dep,
  link_args: host_machine.system() == 'windows' ? '-municode' : [],
  install: true,
)

sndfile_dep = dependency('sndfile', required: false)
if sndfile_dep.found()
  executable('uhjdecoder', 'uhjdecoder.cpp', dependencies: [openal_dep, sndfile_dep])
  executable('uhjencoder', 'uhjencoder.cpp', dependencies: [openal_dep, sndfile_dep])
endif
