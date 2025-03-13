project(groov,
  version: '0.1.0',
  license: 'BSL-1.0',
  languages: 'cpp',
  default_options: ['cpp_std=c++20'])

boost_dep = dependency('boost', required: true)

intel_cbc_sub = subproject('cpp-bare-metal-concurrency')
intel_cbc_dep = cbc_sub.get_variable('cbc_dep')

intel_cse_sub = subproject('cpp-std-extensions')
intel_cse_dep = cse_sub.get_variable('cse_dep')

intel_cbsar_sub = subproject('cpp-baremetal-senders-and-receivers')
intel_cbsar_dep = cbsar_sub.get_variable('cbsar_dep')

intel_sa_sub = subproject('safe-arithmetic')
intel_sa_dep = sa_sub.get_variable('san_dep')

groov_dep = declare_dependency(
  include_directories: groov_inc,
  dependencies: [boost_dep, intel_cbc_dep, intel_cse_dep, intel_cbsar_dep, intel_sa_dep]
  )
