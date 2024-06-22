# Use the latest stable version of the Flutter SDK
FROM cirrusci/flutter:latest

# Set up environment variables for Android SDK
ENV ANDROID_HOME /usr/lib/android-sdk
ENV PATH $PATH:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools

# Install Android SDK
RUN wget -q https://dl.google.com/android/repository/commandlinetools-linux-6609375_latest.zip -O /tmp/cmdline-tools.zip \
    && mkdir -p ${ANDROID_HOME}/cmdline-tools \
    && unzip /tmp/cmdline-tools.zip -d ${ANDROID_HOME}/cmdline-tools \
    && rm /tmp/cmdline-tools.zip

# Accept Android SDK licenses
RUN yes | ${ANDROID_HOME}/cmdline-tools/tools/bin/sdkmanager --licenses

# Install latest Android SDK Platform and Build-Tools
RUN ${ANDROID_HOME}/cmdline-tools/tools/bin/sdkmanager "platform-tools" "platforms;android-30" "build-tools;30.0.3"

# Install additional project-specific tools or libraries if needed
# Placeholder for project-specific installations

# Optimize the container for performance to run smoothly on GitHub Codespaces
# Placeholder for performance optimization steps
