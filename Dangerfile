# github comment settings
github.dismiss_out_of_range_messages

# for PR
if github.pr_title.include? "[WIP]" || github.pr_labels.include?("WIP")
  warn("PR is classed as Work in Progress")
end

# Warn when there is a big PR
fail("a large PR") if git.lines_of_code > 300

# Warn when PR has no assignees
warn("A pull request must have some assignees") if github.pr_json["assignee"].nil?
