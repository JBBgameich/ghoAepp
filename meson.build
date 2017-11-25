# Project Name and Type
project('ghoaepp', 'cpp')

# load and import stuff
conf = configuration_data()
qt5 = import('qt5')

# Config options
conf.set('APPLICATION_ID', '"ga.ghsq.ghoaepp"')
conf.set('APPLICATION_NAME', '"ghoaepp"')
conf.set('APPLICATION_DISPLAY_NAME', '"GHO Äpp"')
conf.set('APPLICATION_DESCRIPTION', '"Ein einfacher Vertretungsplanleser"')

conf.set('VERSION_MAJOR', 0)
conf.set('VERSION_MINOR', 0)
conf.set('VERSION_PATCH', 1)
conf.set('VERSION_EXTRA', '"dev"')
conf.set('VERSION_STRING', '"0.0.1-dev"')

configure_file(output: 'config.h', configuration: conf)

# Dependencies
qt5_modules_deps = dependency('qt5', modules: ['Core', 'Qml', 'Quick', 'Network', 'QuickControls2'])

# Source files
src = ['src/main.cpp', 'src/GHOApp.cpp']
moc_files = qt5.preprocess(qresources: 'qml.qrc', moc_headers: 'src/GHOApp.h')

# Executable
executable('ghoaepp', src, moc_files, dependencies: qt5_modules_deps)
