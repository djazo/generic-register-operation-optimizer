project(groov,
  version: '0.1.0',
  license: 'BSL-1.0',
  languages: 'cpp',
  default_options: ['cpp_std=c++20'])

boost_dep = dependency('boost', required: true)

baremetal_concurrency_sub = subproject('cpp-baremetal-concurrency')
baremetal_concurrency_dep = baremetal_concurrency_sub.get_variable('baremetal_concurrency_dep')

stdx_sub = subproject('cpp-std-extensions')
stdx_dep = cse_sub.get_variable('stdx_dep')

async_sub = subproject('cpp-baremetal-senders-and-receivers')
async_dep = cbsar_sub.get_variable('async_dep')

safe_arithmetic_sub = subproject('safe-arithmetic')
safe_arithmetic_dep = safe_arithmetic_sub.get_variable('safe_arithmetic_dep')

groov_dep = declare_dependency(
  include_directories: groov_inc,
  dependencies: [boost_dep, baremetal_concurrency_dep, stdx_dep, async_dep, safe_arithmetic_dep]
  )
