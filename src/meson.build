labgtk_sources = [
  'main.vala',
  'application.vala',
  'window.vala',
  'content_window.vala',
  'add_data.vala',
  'document/any.vala',
  'document/content.vala',
  'document/document.vala',
  'document/error.vala',
  'document/ioutil.vala',
  'document/metadata.vala',
  'document/type.vala',
  'document/util.vala',
  'document/struct/node.vala',
  'document/struct/nodes.vala',
  'document/keymetadata.vala'
]

posix_dep = meson.get_compiler('vala').find_library('posix')
cc = meson.get_compiler('c')
m_dep = cc.find_library('m', required : false)

labgtk_deps = [
  dependency('gtk4'),
  dependency('sqlite3'),
  dependency('gee-0.8'),
  dependency('gio-2.0'),
  posix_dep, m_dep
]

labgtk_sources += gnome.compile_resources('labgtk-resources',
  'labgtk.gresource.xml',
  c_name: 'labgtk'
)

executable('labgtk', labgtk_sources,
  dependencies: labgtk_deps,
       install: true,
)
