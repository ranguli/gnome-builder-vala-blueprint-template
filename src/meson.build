gnome_builder_vala_blueprint_template_sources = [
  'main.vala',
  'application.vala',
  'window.vala',
]

gnome_builder_vala_blueprint_template_deps = [
  dependency('gtk4'),
  dependency('libadwaita-1', version: '>= 1.2'),
]

blueprints = custom_target('blueprints',
  input: files(
    'window.blp',
    'gtk/help-overlay.blp',
  ),
  output: '.',
  command: [find_program('blueprint-compiler'), 'batch-compile', '@OUTPUT@', '@CURRENT_SOURCE_DIR@', '@INPUT@'],
)

gnome_builder_vala_blueprint_template_sources += gnome.compile_resources('gnome-builder-vala-blueprint-template-resources',
  'gnome-builder-vala-blueprint-template.gresource.xml',
  dependencies: blueprints,
  c_name: 'gnome_builder_vala_blueprint_template',

)

executable('gnome-builder-vala-blueprint-template', gnome_builder_vala_blueprint_template_sources,
  dependencies: gnome_builder_vala_blueprint_template_deps,
       install: true,
)