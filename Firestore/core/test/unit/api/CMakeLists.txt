# Copyright 2019 Google LLC
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#      http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

if(NOT FIREBASE_IOS_BUILD_TESTS)
  return()
endif()

firebase_ios_add_test(
  firestore_api_test
  cc_compilation_test.cc
  load_bundle_task_test.cc
  settings_test.cc
)

target_link_libraries(
  firestore_api_test PRIVATE
  firestore_core
)
