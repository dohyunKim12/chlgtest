node {
 deleteDir()
 sh """
 git clone git@github.com:jenkinsci/git-changelog-plugin.git .
 """

 def changelogString = gitChangelog returnType: 'STRING',
  from: [type: 'REF', value: 'git-changelog-1.50'],
  to: [type: 'REF', value: 'master'],
  template: """
  // Template is documented below!
  """

 currentBuild.description = changelogString
}