# Known bugs and limitations
- Workspace does not scale well in newer operating systems and high dpi.
- Sometimes when opening the contextmenu for a service in ServiceMonitor the menu is
opened for the wrong service.
As a temporary workaround a label is added to the top of the menu showing wich service is
selected.
- Minor GUI problems in Workspace.
- All system stat tags gets qualified to the first node in OPCServer list
- It is not possible to disable diagnostic tags for anything except calculation agent.
- Memory leak in calculation. As temporary workaround the ChaosMonkey can be used to
restart the agents at desired interval.
# Releases
## 3.3.0
### New features
- Compression analyzer: New tool for reviewing and configuring compression settings.
- New test platform for long running tests, Long running platform.
- Upgraded IronPython (used in python calculations) from version 2.7.3 to 2.7.8
- Improved performance of XMZ export from databases with large dbo.Change tables.
- Database patch 3.0.1.06
- ServiceMonitor genereates a default config if requested config file does not exist, #153
- Configuration dialogs in ServiceMonitor is not modal anymore, #155
- Improved zoom in trends with high density of values, #149
- Major performance improvement of XY Plot, #233
- Multiple improvements of TagValueGrid, #252
- Listing third party components in About dialog according to their MIT licenses, #140
- Values imported from Excel gets AAManual quality, #244
- Excluded unnecessary files from setup packages to reduce size, #248
- Button too freeze the grid when adding or changing items in Admin, #151
- GetLogValues method in RestProvider, #215
- Possible to disable the "Save Workspace" dialog when closing the Workspace, #209
- DataAdapters now fully support collection of double precision, #211
- MaxDivergence is always set to 0.5% of specified range, #191
- Major improvement of memory usage in Workspace, #208
- All event filters are available in combo box above grid, #182
- TimeSelector Offset is disabled when not in any timegroup, #183
### Fixed bugs
- Solved a memory leak in Calculation agent
- Installation of AutArch Workspace adds the correct user rights to the installation folder,
#146
- ServiceMonitor configuration file is always created in the installation folder
- Events were not removed from the event grid in live mode, #158
- Values were not removed from TagValueGrid in live mode, #189
- Live subscription of events did not stop when closing event grid, #159
- Unexpected behaviour when adding or subtracting time over a DST-shifting, #162
- User did not get sufficient rights to database jobs, #251, #239
- Workspace could crash when editing a dashboard before it was fully loaded, #249
- ReportGenerator failed to generate report if the template was open in Excel, #178
- TagValueGrid could stop working in live, #207, #210
- XY Plot could stop working in live, #160, #157
- Radar Plot could stop working in live, #156
- An old value could get repeated by SigForceUpdate, #213
- TimeGroup with TagValueGrid did not work, #193
- EventGrid menu of selected columns was not correct when opening saved workspace, #92
- Improved selection of EventGrid columns, #91
## 3.2.8
### New features
- System alarm check at startup is configurable, #129.
- SQL Patch 3.0.1.03
- Max sweep size configurable for Calculation agent.
- Max end time configurable for Calculation agent.
- Excel export includes milliseconds in timestamps.
- Opening a default config in ServiceMonitor if requested config does not exist.
### Fixed bugs
- Tags not added to plugin when starting workspace from command line, #130.
- Workspace does not appear on top when started, #126.
- Calculation agent stopped progressing in time, #132.
- TimePeriod and AADateTime is configurable in ServiceMonitor.
## 3.2.7
### New features
### Fixed bugs
- Fixed problems in XMZ export.
## 3.2.6
### New features
- Improved data fetching performance.
- Improved Calculation agent performance.
- Improved recalc performance.
- Start ClickOnce published Workspace with arguments.
- Multi-value html editor.
- Machine learning agent.
- Machine learning training html ui.
- Updated codesign certificate.
- Improved data fetching performance
### Fixed bugs
## 3.2.5
### New features
- Event filter for OPCAE and OPCUA.
### Fixed bugs
## 3.2.4
### New features
### Fixed bugs
- Fixed problems in XMZ export.
## 3.2.3
### New features
### Fixed bugs
- Fixed problems in XMZ export.
## 3.2.2
### New features
- Database patch 3.0.0.16.
- Moved columns in the Admin tool.
- Possible to store a custom config for report StandardTemplate.
- Timestamps in report includes milliseconds.
- Password dialog for admin tools in Workspace.
- Rename of tags supported in Admin tool.
- Can insert a comment when importing excel values.
- Possibility to exclude multiple clients from AutArch Status.
- Possibility to set allowed diff time individually in AutArch Status.
### Fixed bugs
- Multiple GUI fixes in Workspace.
- Multiple GUI fixes in report excel template.
- File association with Workspace files (.aaws) was not working.
- It was not possible to disable diagnostic tags for calculation agent.
- StandardTemplate for report was not imported correctly with GlobalUpdate.
- Caclculation agents with COB calculations could run intervals smaller than configured
amount.
- Calculations stored from Python editor got wrong end time.
- Supervision server could restart a service that was currently starting.
- Log all command from ServiceMonitor was not working.
- XY-plot works in live mode.
- XMZ export could possible create an incorrect end interpolated value.
## 3.2.1
### New features
### Fixed bugs
- OPCDA Client sometimes attempted to reconnect to the server while the client was shutting
down.
- Multiple GUI fixes in Workspace.
## 3.2.0
### New features
- Dashboard officially supported.
- Report officially supported.
- LiveExcel officially supported.
- New GUI and official support for Excel export/import.
- Database version 3.0.0.13
- Event subscription through OPCUA.
- New setup package for AutArch database with SQL 2014
- MultiValue tags.
- GlobalUpdate can now be used to patch database and is replacing
AutArchDatabasePatcher.
(AutArchDatabasePatcher is still working but will not be maintained)
- OPCServer and OPCGroup configuration in Admin are equalized with other tabs.
- Admin search is using wildcards instead of regex.
- User-friendly configuration dialog when installing ClickOnce Workspace.
### Fixed bugs
- CalculationAgent config sometimes gets corrupted.
- Comparison of datetime rounded to SqlDatetime gave unexpected result.
- Memory leak in CalculationAgent.
- SupervisionServer does not automatically set itself to auto-start.
- Adapter awaits broker connection for 10 seconds at startup before reading offline config.
- Calculation of tags with property ExtendLastValue produced incorrect values.
- OPCAE Recording Node did not run SigForceUpdate which caused AutArch Status to
alarm.
- Minor GUI improvements in AutArch Workspace.
## 3.1.2
### New features
- Database version 3.0.0.08
### Fixed bugs
- Not polling values for tags with subscription problems.
- Extra poll attempt after successfully setting up subscriptions.
- Reduced unnecessary logging.
- Memory leak in CaclulationAgent.
## 3.1.1
### New features
Last value only stays in collector service for max 10 minutes #41
### Fixed bugs
- Validation of the value insurance platform is not working.
## 3.1.0
### New features
- Calculation Agent is now fully tested and approved
- All RecordingNodes poll values for all tags when started
- Improved Broker performance
- Cleaned all configuration files so that they only contain what is necessary.
- Added comments to configuration files
- AutArch components logs their own errors to eventlog in database.
- Database version 3.0.0.04
### Fixed bugs
- Invallid char in XMZ Export, #23
- Error serializing TuneStatusEnum in offline config, #25
- Error serializing PythonInof in offline config, #2
## 3.0.0
### New features
- Improved performance and resolved bugs by moving calculations from the DataBroker to
CalculationAgent.
- To make installation simpler all nodes are now hosted in a CentralServices
- The old Admin application is completely replaced by the new tool included in Workspace.
- Improved test coverage with new testplatforms
### Fixed bugs
- Problems with calculation order of Python calculations
- Performance issues in DataBroker
## 2.0.0
### New features
- Complete rebuild of Service Framework including new OPC clients
- OPCClients can react on new tag configuration and apply it in runtime without restart
- S7Adapter (fastlogger) used for faster sampling of values from Siemens S7 systems
- Redundant adapters/brokers
- Easier creation of aggregated tags
- Calculations written in Python
### Fixed bugs
